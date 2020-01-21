<template>
    <header class="header" ref='header' :class="headerFixed">
        <div class="container">
            <h1>Tk Portfolio</h1>

            <nav>
                <ul class="gnav">
                    <li><nuxt-link :class="headerFixed" active-class="link-active" to="/" exact>Home</nuxt-link></li>
                    <li><nuxt-link :class="headerFixed" active-class="link-active"  to="/works">Works</nuxt-link></li>
                    <li><nuxt-link :class="headerFixed" active-class="link-active"  to="/contact">Contact</nuxt-link></li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
export default {
    data() {
        return {
            headerHeight: '',
            windowHeight: '',
            headerFixed: null
        }
    },
    mounted() {
        this.headerHeight = this.$refs.header.clientHeight
        window.addEventListener('scroll', this.scrollWindow)
    },
    methods: {
        scrollWindow(){
            this.windowHeight = window.scrollY
            if(this.headerHeight < this.windowHeight) {
                this.headerFixed = 'headerFixed'
            }else {
                this.headerFixed = null
            }
        }
    }
}
</script>

<style lang="scss" scoped>

.header {
    padding: 30px 20px;
    box-sizing: border-box;
    box-shadow: 0 0 2px #333;
    position: fixed;
    width: 100%;
    z-index: 9999;
    .container {
        display: flex;
        justify-content: space-between;
        align-items: flex-end;
        .gnav {
            display: flex;
            justify-content: space-between;
            & li:not(:last-of-type){
                margin-right: 20px;
            }
        }
    }
}

.headerFixed {
    background: rgba(24, 24, 24, 0.8);
    color: #fff;
    .link-active {
        border-bottom-color: #fff;
    }
}

.link-active {
    border-bottom: 2px solid black; 
}

</style>