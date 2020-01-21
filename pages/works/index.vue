<template>
    
    <transition>
        <div>
            <keyvisualSection />
            <section id="works-area">ddddddddddddd</section>

            <p>gagagag</p>
            <p>agagaga</p>
        </div>
    </transition>
  
</template>

<script>
import keyvisualSection from '~/components/keyvisual.vue'
export default {
    components: {
        keyvisualSection
    }
}
</script>


<style lang="scss">
.page-enter {
  transform: translate(-100px, 0);
  opacity: 0;
}
.page-enter-to {
  opacity: 1;
}
.page-enter-active {
  transition: all 1s 0s ease;
}
.page-leave {
  transform: translate(0, 0);
  opacity: 1;
}
.page-leave-to {
  transform: translate(100px, 0);
  opacity: 0;
}
.page-leave-active {
  transition: all .5s 0s ease;
}


section {
  padding: 30px 0;
  box-sizing: border-box;
}
</style>