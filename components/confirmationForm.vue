<template>
        <form >
            <div class="form-outer">
                <label for="confirmationForm-name">お名前</label>
                <input id="confirmationForm-name" type="text" readonly  v-model="inputContent.name">
            </div>

            <div class="form-outer">
                <label for="confirmationForm-email">アドレス</label>
                <input id="confirmationForm-email" type="email" readonly v-model="inputContent.email">
            </div>

            <div class="form-outer">
                <label for="confirmationForm-text">お問い合わせ</label>
                <textarea name="text" id="confirmationForm-text" cols="30" rows="10" readonly v-model="inputContent.text"></textarea>
            </div>

            <p><button class="send-btn" type="submit">送信</button></p>
            <p class="return-btn" @click="returnForm">戻る</p>
        </form>
</template>

<script>
export default{
    props:['inputContent'],
    methods: {
        returnForm() {
            this.$emit('returnForm')
        }
    }
}
</script>

<style lang="scss" scoped>


.form-outer {
    width: 100%;
    margin-bottom: 30px;
    & label {
        display: block;
        border-left: 5px solid #333;
        padding-left: 10px;  
        margin-bottom: 10px;
    }
    & input, textarea {
        width: 100%;
        border-radius: 0;
        border: none;
        outline: none;
        font-family: inherit;
        font-size: inherit;
        text-indent: 1.4rem;
    }
    & input {
        line-height: 2rem;
        height: 2rem;
    }
    & textarea {
        resize: none;
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

.return-btn {
    width: 100%;
    color: #fff;
    background: rgb(255, 161, 161);
    padding: 20px 0;
    text-align: center;
    cursor: pointer;
    
}
</style>