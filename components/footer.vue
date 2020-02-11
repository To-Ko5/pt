<template>
    <footer class="footer">
        <div class="container">
            <p><small>TK Portfolio</small></p>
            <p v-show="windowHeight > 100" class="top-btn" @click="returnTop">Top</p>
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
            const duration = 400;  // 移動速度
            const interval = 10;    // 移動間隔
            const step = -window.scrollY / Math.ceil(duration / interval); // 1回に移動する距離
            const timer = setInterval(() => {
                    window.scrollBy(0, step);   
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
        background: #000;
        color: #fff;
        text-align: center;
        padding: 30px 0;
    }

    .top-btn {
        position: fixed;
        bottom: 10px;
        right: 10px;
        width: 50px;
        height: 50px;
        line-height: 50px;
        border-radius: 4px;
        background: #333;
        color: #fff;
        cursor: pointer;
    }
</style>