<template>
  <transition>
    <div>
      <ContactKeyvisual />
      <section id="form" class="section-area form">
        <formSection />
      </section>
    </div>
  </transition>
</template>

<script>
import ContactKeyvisual from "~/components/ContactKeyvisual.vue";
import formSection from "~/components/form.vue";
export default {
  components: {
    ContactKeyvisual,
    formSection
  }
};
</script>

<style lang="scss" scoped>
.form {
  background: #fafafa;
}
</style>