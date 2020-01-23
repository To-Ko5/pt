<template>
  <div>
    <headerSection />
    <div class="contents">
      <nuxt />
    </div>
    <footerSection />
  </div>
</template>


<script>
import headerSection from '~/components/header.vue'
import footerSection from '~/components/footer.vue'

export default {
  components: {
    headerSection,
    footerSection
  }
}
</script>

<style lang="scss">
html,body,h1,h2,h3,ul,li,p {
   margin: 0;
   padding: 0;
   line-height: 1.0;
}

ul {
    list-style: none;
}
a {
    text-decoration: none;
    color: inherit;
}

table {
border-collapse: collapse;
border-spacing: 0;
}

img {
    border: none;
    vertical-align: bottom;
    max-width: 100%;
    height: auto;
}
/* reset */
html {
    font-size: 62.5%;
}

body {
   font-size: 1.6rem;
   color: #333;
   background: #fffefe;
   font-weight: 500;
   font-family: 'Noto Sans JP', sans-serif;
}

.container {
  max-width: 960px;
  margin: 0 auto;
}

.contents {
  padding-top: 92px;
}

.section-area {
  padding: 50px 0;
  box-sizing: border-box;
}

h2 {
    text-align: center;
    margin-bottom: 40px;
    font-size: 4rem;
}

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
</style>
