<template>
  <div class="keyvisual">
    <p class="keyvisual-title">Works</p>
  </div>
</template>

<style lang="scss" scoped>
.keyvisual {
  height: calc(100vh - 100px);
  width: 100%;
  background: no-repeat url("~@/assets/works.jpg") left 30% center / cover;
  position: relative;
  .keyvisual-title {
    position: absolute;
    font-size: 10rem;
    top: 40%;
    left: 50%;
    transform: translate(-50%, -40%);
  }
}

@media screen and (max-width: 968px) {
  .keyvisual {
    height: calc(100vh - 66px);
    .keyvisual-title {
      font-size: 5rem;
    }
  }
}
</style>