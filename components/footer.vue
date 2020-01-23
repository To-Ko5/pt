<template>
    <footer class="footer">
        <div class="container">
            <p><small>Tk Portfolio</small></p>
            <p v-show="windowHeight > 100" class="top-btn" @click="returnTop">top</p>
        </div>
    </footer>
</template>


<script>
 export default {
     data(){
         return {
             headerHeight: '',
             windowHeight: ''
         }
     },
     mounted(){
        window.addEventListener('scroll',this.scrollWindow)
     },
     methods: {
         scrollWindow(){
             this.windowHeight = window.scrollY
         },
         returnTop(){
            const duration = 400;  // 移動速度（1秒で終了）
            const interval = 10;    // 0.025秒ごとに移動
            const step = -window.scrollY / Math.ceil(duration / interval); // 1回に移動する距離
            const timer = setInterval(() => {
                    window.scrollBy(0, step);   // スクロール位置を移動
                    if(window.scrollY <= 0) {
                        clearInterval(timer);
                    }
                },interval);

         }
     }
 }
</script>

<style lang="scss" scoped>
    .footer {
        background: #efefef;
        text-align: center;
        padding: 20px 0;
    }

    .top-btn {
        position: fixed;
        bottom: 0;
        right: 0;
        width: 50px;
        height: 50px;
        line-height: 50px;
        background: #333;
        color: #fff;
    }
</style>