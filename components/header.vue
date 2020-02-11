<template>
    <header class="header" ref='header' :class="headerFixed">
        <div class="container">
            <h1 class="main-title">TK Portfolio</h1>

            <nav v-if="windowWidth > 968">
                <ul class="gnav">
                    <li><nuxt-link :class="gnavFixed"  active-class="link-active" to="/" exact>Home</nuxt-link></li>
                    <li><nuxt-link :class="gnavFixed"  active-class="link-active"  to="/works">Works</nuxt-link></li>
                    <li><nuxt-link :class="gnavFixed" active-class="link-active"  to="/contact">Contact</nuxt-link></li>
                </ul>
            </nav>

            <div v-else class="sp-nav-btn" @click="spNavClick">
                <i class="fas fa-times" v-if="spNavFlag"></i>
                <i class="fas fa-bars" v-else></i>
            </div>
        </div>
    </header>
</template>

<script>

export default {
    props: ['spNavFlag'],
    data() {
        return {
            headerHeight: '',
            windowHeight: '',
            windowWidth: '',
            headerFixed: null,
            gnavFixed: null,
            nowFixed: false,
            spNavBtnState: true
        }
    },
    mounted() {
        this.windowWidth = window.innerWidth
        this.headerHeight = this.$refs.header.clientHeight
        window.addEventListener('scroll', this.scrollWindow)
    },
    methods: {
        scrollWindow(){
            this.windowHeight = window.scrollY
            if(this.headerHeight < this.windowHeight) {
                this.headerFixed = 'header-fixed'
                this.gnavFixed = 'gnav-fixed'
                this.nowFixed = false
            }else {
                this.headerFixed = null
                this.gnavFixed = null
            }

            if(this.nowFixed){
                this.headerFixed = 'header-fixed'
                this.gnavFixed = 'gnav-fixed'
            }
        },
        spNavClick() {
            this.$emit("clickSpNav")
        }
    },
    watch: {
        '$route'(){
            if(this.headerFixed) {
                this.nowFixed = true
            }
        }
    }
}
</script>

<style lang="scss" scoped>

.header {
    padding: 30px 0;
    box-sizing: border-box;
    box-shadow: 0 0 2px #333;
    position: fixed;
    width: 100%;
    z-index: 98;
    .container {
        display: flex;
        justify-content: space-between;
        align-items: flex-end;
        .main-title {
            font-size: 4rem;
        }
        .gnav {
            display: flex;
            justify-content: space-between;
            & li:not(:last-of-type){
                margin-right: 20px;
            }
            & a:hover {
                border-bottom: 2px solid black;
                transition: .2s;
            }
            & a:hover.gnav-fixed {
                border-bottom-color:#fff;
            }
        }
    }
}


.header-fixed {
    transition: .3s;
    background: rgba(24, 24, 24, 0.9);
    color: #fff;
}


.link-active.gnav-fixed {
    border-bottom: 2px solid #fff; 
}


.link-active {
    border-bottom: 2px solid black; 
}

@media screen and (max-width: 968px) {
    .header {
        padding: 20px 0;
        .container{
            display: block;
            text-align: center;
            .main-title {
                font-size: 2.6rem;
            }
        }
    }
}

.sp-nav-btn {
    position: absolute;
    top: 10px;
    right: 10px;
    font-size: 3rem;
}

</style>