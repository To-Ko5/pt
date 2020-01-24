<template>
    <div>
        <ul class="sp-nav" v-if="spNavFlag">
            <li><nuxt-link  active-class="link-active" to="/" exact>Home</nuxt-link></li>
            <li><nuxt-link  active-class="link-active"  to="/works">Works</nuxt-link></li>
            <li><nuxt-link  active-class="link-active"  to="/contact">Contact</nuxt-link></li>
        </ul>

        <p class="sp-nav-btn" @click="spBtnClick">MENU</p>
    </div>
</template>


<script>
export default {
    data(){
        return {
            spNavFlag: false
        }
    },
    methods: {
        spBtnClick(){
            this.spNavFlag = !this.spNavFlag
        }
    }
}
</script>


<style lang="scss" scoped>
    .sp-nav {
        position: fixed;
        width: 100%;
        height: 100vh;
        z-index: 9999;
        & li {
            height: calc(100vh/3);
            background: red;
        } 
    }
</style>