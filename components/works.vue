<template>
    <div class="container">
        <h2>works</h2>
        <div class="works-area">
            <div class="works-content">
                <div class="img-effect">
                    <img src="~/assets/login.PNG" >
                </div>
            </div>
            <div class="works-content">
                <div class="img-effect">
                    <img src="~/assets/login.PNG" >
                </div>
            </div>
            <div class="works-content">
                <div class="img-effect">
                    <img src="~/assets/login.PNG" >
                </div>
            </div>
            <div class="works-content">
                <div class="img-effect">
                    <img src="~/assets/login.PNG" >
                </div>
            </div>
            <div class="works-content">
                <div class="img-effect">
                    <img src="~/assets/login.PNG" >
                </div>
            </div>
            <div class="works-content">
                <div class="img-effect">
                    <img src="~/assets/login.PNG" >
                </div>
            </div>
        </div>

        <p><nuxt-link to="/works/#works-area">view more</nuxt-link></p>
    </div>
</template>


<style lang="scss" scoped>

.works-area {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    .works-content {
        width: 30%;
        overflow: hidden;
        .img-effect {
            position: relative;
            width: 300px;
            height: 180px;
            transition-duration: 0.3s;
            &:hover {
                transform: scale(1.1);
                &:before {
                    opacity: 1;
                    transform: scale(1.3); /* 文字の拡大率 */
                    filter: blur(0);
                }
            }
            &:before {
                content: "UP";
                position: absolute;
                width: 300px;
                height: 180px;
                background: radial-gradient(rgba(0, 0, 0, 0.2), rgba(0, 0, 0, 0.8)); /* 円形グラデーション */
                transition-duration: 0.3s;
                opacity: 0; /* 見えないように透過しておく */
                display: flex; /* 文字の中央配置 */
                justify-content: center; /* 文字の中央配置 */
                align-items: center; /* 文字の中央配置 */
                color: #fff;
                font-size: 22px;
                text-shadow: 0 0 2px #000;
                filter: blur(4px); /* ブラー効果 */
            }
        }
    }
}
</style>