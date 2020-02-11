<template>
    <div class="container" >
        <h2>お問い合わせ</h2>
        <div class="form-area">
            <form @submit.prevent="confirmationSubmit">
                <div class="form-outer">
                    <label for="name">お名前<span class="required-span">※必須</span></label>
                    <input id="name" type="text" v-model.trim="inputContent.name">
                    <p class="error-message" v-if="errorMessageFlag.name">名前を入力してください</p>
                </div>

                <div class="form-outer">
                    <label for="email">アドレス<span class="required-span">※必須</span></label>
                    <input id="email" type="email" v-model.trim="inputContent.email" >
                    <p class="error-message" v-if="errorMessageFlag.email">アドレスを入力してください。</p>
                </div>

                <div class="form-outer">
                    <label for="text">お問い合わせ<span class="required-span">※必須</span></label>
                    <textarea name="text" id="text" cols="30" rows="10" v-model.trim="inputContent.text" ></textarea>
                    <p class="error-message" v-if="errorMessageFlag.text">お問い合わせ内容を入力してください</p>
                </div>

                <p><button class="send-btn" type="submit">送信内容の確認</button></p>
            </form>
        </div>

        <client-only>
            <modal name="modal-content"  width="80%" height="auto" :scrollable="true">
                <confirmationForm @returnForm="canselForm" :inputContent="inputContent" />
            </modal>
        </client-only>            
    </div>
</template>


<script>
import confirmationForm from '~/components/confirmationForm'

export default {
    components: {
        confirmationForm
    },
    data(){
        return{
            inputContent: {
                name: '',
                email: '',
                text: '',
            },
            errorMessageFlag: {
                name: '',
                email: '',
                text: ''
            }
        }
    },
    methods: {
        confirmationSubmit(){
            
            if(!this.inputContent.name || !this.inputContent.name.match(/\S/g)){
                this.errorMessageFlag.name = true
                return
            }else {
                this.errorMessageFlag.name = false
            }

            if(!this.inputContent.email || !this.inputContent.email.match(/\S/g)){
                this.errorMessageFlag.email = true
                return
            }else {
                this.errorMessageFlag.email = false
            }
            
           if(!this.inputContent.text || !this.inputContent.text.match(/\S/g)){
                this.errorMessageFlag.text = true
                return
            }else {
                this.errorMessageFlag.text = false
            }            
            this.$modal.show("modal-content");
        },
        canselForm(){
            this.$modal.hide("modal-content");
        }
    }
}

</script>



<style lang="scss" scoped>

.form-area {
    max-width: 500px;
    margin: 0 auto;
}

.form-outer {
    margin-bottom: 30px;
    & label {
        display: block;
        margin-bottom: 10px;
        .required-span {
            color:rgb(255, 81, 81);
            font-weight: 400;
            font-size: 1.3rem;
            margin-left: 10px; 
        }
    }
    & input, textarea {
        width: 100%;
        appearance: none;
        border: none;
        outline: none;
        font-family: inherit;
        font-size: inherit;
        background: #fff;
        box-shadow: 1px 1px 2px rgba(51, 51, 51, 0.301);
        &:focus {
            background: rgb(239, 253, 255);
        }
    }
    & input {
        line-height: 4rem;
        height: 4rem;
    }
    & textarea {
        resize: none;
    }
}

.send-btn {
    width: 100%;
    color: #fff;
    padding: 20px 0;
    border: none;
    cursor: pointer;
    outline: none;
    appearance: none;
    text-decoration: none;
    background: #668ad8;
    border-bottom: solid 4px #627295;
    border-radius: 3px;
    font-size: inherit;
    font-family: inherit;
}

.error-message  {
    color: rgb(255, 81, 81);
    margin-top: 8px;
}

</style>