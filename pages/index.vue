<template>
  <div>
    <MainKeyvisualSection />
    <section class="section-area about"> 
      <AboutSection />
    </section>
    <section class="section-area skills"> 
      <SkillSection />
    </section>
    <section class="section-area works">
      <WorksSection />
    </section>
    <section class="section-area contact">
      <ContactSection />
    </section> 
  </div>
</template>

<script>
import MainKeyvisualSection from '~/components/MainKeyvisual.vue'
import AboutSection from '~/components/About.vue'
import SkillSection from '~/components/Skill.vue'
import WorksSection from '~/components/Works.vue'
import ContactSection from '~/components/Contact.vue'

export default {
  components: {
    MainKeyvisualSection,
    AboutSection,
    SkillSection,
    WorksSection,
    ContactSection
  }
}
</script>

<style lang="scss" scoped>


.skills {
  background:linear-gradient(rgba(236, 255, 250, 0.4),rgba(248, 255, 255, 0.4),rgba(252, 255, 255, 0.4)),
  no-repeat url('~@/assets/skillbg.jpg') center/cover;
}

.contact {
  background: #efefef;
}

</style>

