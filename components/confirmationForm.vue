<template>
  <div class="confirmation-form-outer">
    <form
      action="https://docs.google.com/forms/u/1/d/e/1FAIpQLSdA3Ntb26H0u58glAyUmRg9hqDfP1zbPlapJ1_q1FZX7xZn5w/formResponse"
    >
      <div class="form-outer">
        <label for="confirmationForm-name">お名前</label>
        <input
          id="confirmationForm-name"
          type="text"
          readonly
          v-model="inputContent.name"
          name="entry.2005620554"
        />
      </div>

      <div class="form-outer">
        <label for="confirmationForm-email">アドレス</label>
        <input
          id="confirmationForm-email"
          type="email"
          readonly
          v-model="inputContent.email"
          name="entry.1045781291"
        />
      </div>

      <div class="form-outer">
        <label for="confirmationForm-text">お問い合わせ</label>
        <textarea
          name="entry.839337160"
          id="confirmationForm-text"
          cols="20"
          rows="10"
          readonly
          v-model="inputContent.text"
        ></textarea>
      </div>

      <p>
        <button class="send-btn" type="submit">送信</button>
      </p>
      <p class="return-btn" @click="returnForm">戻る</p>
    </form>
  </div>
</template>

<script>
export default {
  props: ["inputContent"],
  methods: {
    returnForm() {
      this.$emit("returnForm");
    }
  }
};
</script>

<style lang="scss" scoped>
.confirmation-form-outer {
  padding: 40px;
  box-sizing: border-box;
}

.form-outer {
  width: 100%;
  margin-bottom: 30px;
  & label {
    display: block;
    border-left: 5px solid #333;
    padding-left: 10px;
    margin-bottom: 10px;
  }
  & input,
  textarea {
    width: 100%;
    border-radius: 0;
    border: none;
    outline: none;
    font-family: inherit;
    font-size: inherit;
    text-indent: 1.4rem;
  }
  & input {
    line-height: 2.4rem;
    height: 2.4rem;
  }
  & textarea {
    resize: none;
    overflow: auto;
  }
}

.send-btn,
.return-btn {
  width: 30%;
  min-width: 180px;
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
  text-align: center;
  display: block;
  margin: 0 auto;
}

.return-btn {
  background: rgb(255, 161, 161);
  border-bottom: solid 4px rgb(255, 134, 134);
  margin-top: 20px;
}
</style>