<template>
    <div class="keyvisual">
        <p class="keyvisual-title">Portfolio</p>
    </div>
</template>

<style lang="scss" scoped>
.keyvisual{
    height: calc(100vh - 91.11px);
    width: 100%;
    background: no-repeat url("~@/assets/keyvisual.jpg") right 46% bottom/cover;
    background-attachment: fixed;
    position: relative;
    .keyvisual-title {
        position: absolute;
        top: 10%;
        left: 50%;
        transform: translate(-50%,-10%);
        font-size: 40rem;
    }
}
</style>


