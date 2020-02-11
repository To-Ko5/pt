<template>
  <div>
    <HeaderSection @clickSpNav="clickSpNav" :spNavFlag="spNavFlag" />
    <template v-if="spNavFlag">
      <Spnav @clickSpNav="clickSpNav" />
    </template>
    <div class="main-contents">
      <nuxt />
    </div>
    <FooterSection />
  </div>
</template>


<script>
import HeaderSection from '~/components/Header.vue'
import FooterSection from '~/components/Footer.vue'
import Spnav from '~/components/Spnav.vue'

export default {
  data() {
    return{
      spNavFlag: false
    }
  },
  components: {
    HeaderSection,
    Spnav,
    FooterSection
  },
  methods: {
    clickSpNav(){
      this.spNavFlag = !this.spNavFlag
    }
  },
  watch: {
    '$route'(){
        if(this.spNavFlag) {
            this.spNavFlag = false
        }
     }
  },
}
</script>

