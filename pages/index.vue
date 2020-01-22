<template>
  <div>
    <keyvisual-section />
    <section class="about"> 
      <about-section />
    </section>
    <section class="about"> 
      <skill-section />
    </section>
    <section class="works">
      <worksSection />
    </section>
    <section class="contact">
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

<style>

</style>
