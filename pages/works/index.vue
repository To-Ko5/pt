<template>
  <transition>
    <div>
      <WorksKeyvisual />
      <section id="works" class="section-area">
        <WorksPage />
      </section>
    </div>
  </transition>
</template>

<script>
import WorksKeyvisual from "~/components/WorksKeyvisual.vue";
import WorksPage from "~/components/WorksPage.vue";
export default {
  components: {
    WorksKeyvisual,
    WorksPage
  }
};
</script>
