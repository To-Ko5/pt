<template>
  <div>
    <keyvisual-section />
    <section class="section-area about"> 
      <about-section />
    </section>
    <section class="section-area skills"> 
      <skill-section />
    </section>
    <section class="section-area works">
      <worksSection />
    </section>
    <section class="section-area contact">
      <contactSection />
    </section> 
  </div>
</template>

<script>
import keyvisualSection from '~/components/keyvisual.vue'
import aboutSection from '~/components/about.vue'
import skillSection from '~/components/skill.vue'
import worksSection from '~/components/works.vue'
import contactSection from '~/components/contact.vue'

export default {
  components: {
    keyvisualSection,
    aboutSection,
    skillSection,
    worksSection,
    contactSection
  }
}
</script>

<style lang="scss" scoped>
.about {
  background: linear-gradient(rgba(249, 255, 255, 0.4),rgba(255, 230, 230, 0.4), rgba(255, 217, 210, 0.4)), no-repeat url('~@/assets/building.jpg') 90% top/cover fixed;
}

.skills {
  background:linear-gradient(rgba(255, 217, 210, 0.4),rgba(255, 241, 241, 0.4),rgba(249, 255, 255, 0.4)), no-repeat url('~@/assets/building2.jpg') center top/cover fixed;
}

.works {
  background: linear-gradient(rgb(246, 255, 255),rgb(230, 255, 255), rgb(190, 236, 248));
}
</style>

