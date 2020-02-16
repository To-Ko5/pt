<template>
  <div class="container">
    <h2>Contact</h2>
    <p class="btn-area">
      <nuxt-link to="/contact/#form">お問い合わせはこちら</nuxt-link>
    </p>
  </div>
</template>

<style lang="scss" scoped>
.btn-area {
  width: 300px;
  margin: 0 auto;
  text-align: center;
  & a {
    display: inline-block;
    width: 100%;
    text-align: center;
    color: black;
    text-decoration: none;
    font-weight: bold;
    padding: 20px;
    box-sizing: border-box;
    position: relative;
    border: 2px solid black;
    transition: 0.4s;
    &:hover {
      border: 2px solid transparent;
      color: rgb(19, 102, 255);
      &:after,
      &:before {
        transform: scale(1);
      }
    }
    &:before,
    &:after {
      width: 100%;
      height: 100%;
      z-index: 3;
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      box-sizing: border-box;
      transform: scale(0);
      transition: 0.2s;
    }
    &:before {
      border-bottom: 2px solid rgb(19, 102, 255);
      border-left: 2px solid rgb(19, 102, 255);
      transform-origin: 100% 0%;
    }
    &:after {
      border-top: 2px solid rgb(19, 102, 255);
      border-right: 2px solid rgb(19, 102, 255);
      transform-origin: 0% 100%;
    }
  }
}

@media screen and (max-width: 768px) {
  .btn-area {
    width: 220px;
  }
}
</style>