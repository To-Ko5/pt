<template>
    <div class="container">
        <h2>works</h2>
        <div class="works-area">
            <div class="works-content">
                <nuxt-link to="dd">
                    <div class="img-effect">
                         <img src="~/assets/login.PNG">
                    </div>
                </nuxt-link>
            </div>
        </div>


        <p class="view-more-btn-outer">
            <nuxt-link to="/works/#works-area" class="view-more-btn">view more</nuxt-link>
        </p>
    </div>
</template>

<script>

import work1 from '~/components/work1.vue'
import work2 from '~/components/work2.vue'

export default {
    components: {
        work1
    },
}
</script>


<style lang="scss" scoped>

.works-area {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    margin-bottom: 30px;
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


.view-more-btn-outer{
    width: 300px;
    margin: 0 auto;
    .view-more-btn {
    display: block;
    text-align: center;
    border: 2px solid #9ec34b;
    color: #9ec34b;
    text-decoration: none;
    font-weight: bold;
    padding: 20px 0;
    border-radius: 4px;
    transition: .4s;
    &:hover{
        background-color: #9ec34b;
        border-color: #cbe585;
        color: #FFF;
        }
    }
} 

</style>