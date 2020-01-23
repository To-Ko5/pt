<template>
    <div class="container" >
        <h2>お問い合わせ</h2>
        <transition>
        <div class="modal" :class="modalOverlay" >
            <div v-if="formFlagBefore" class="form-area">
                <form @submit.prevent="confirmationSubmit">
                    <div class="form-outer">
                        <label for="name">お名前</label>
                        <input id="name" type="text" v-model="inputContent.name">
                    </div>

                    <div class="form-outer">
                        <label for="email">アドレス</label>
                        <input id="email" type="email" v-model="inputContent.email">
                    </div>

                    <div class="form-outer">
                        <label for="text">お問い合わせ</label>
                        <textarea name="text" id="text" cols="30" rows="10" v-model="inputContent.text"></textarea>
                    </div>

                    <p><button class="send-btn" type="submit" >送信内容の確認</button></p>
                </form>
            </div>

            <div v-else class="confirmation-form-area">
                <confirmationForm @returnForm="canselForm" :inputContent="inputContent" />
            </div>
        </div>
        </transition>
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
            formFlagBefore: true, 
            modalOverlay: null,
            inputContent: {
                name: '',
                email: '',
                text: '',
            },
        }
    },

    methods: {
        confirmationSubmit(){
            this.formFlagBefore = !this.formFlagBefore
            this.modalOverlay = 'modal-overlay'
        },
        canselForm(){
            this.modalOverlay = null
            this.formFlagBefore = true
            this.$router.push('/contact/#form')
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
    }
    & input, textarea {
        width: 100%;
    }
    & input {
        line-height: 2rem;
        height: 2rem;
    }
}

.send-btn {
    width: 100%;
    color: #fff;
    background: black;
    padding: 20px 0;
    border: none;
    cursor: pointer;
    outline: none;
    appearance: none;
}


.modal-overlay {
    position: fixed;
    top: 0;
    left: 0;
    background: rgba(0, 0, 0, 0.945);
    width: 100%;
    height: 100%;
    z-index: 9998;
    .confirmation-form-area {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%,-50%);
        width: 60%;
        background: #fff;
        padding: 40px;
        box-sizing: border-box;
        z-index: 9999;
    }
}

</style>