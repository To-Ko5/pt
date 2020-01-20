<template>
  <div>
    <headerSection/>
    <nuxt />
  </div>
</template>


<script>
import header from '~/components/header.vue'
export default {
  components: {
    headerSection: header
  }
}
</script>

<style lang="scss">
html,body,h1,h2,h3,ul,li {
   margin: 0;
   padding: 0;
   line-height: 1.0;
}

ul {
    list-style: none;
}
a {
    text-decoration: none;
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
   font-weight: 500;
   font-family: 'Noto Sans JP', sans-serif;
}

.container {
  max-width: 960px;
  margin: 0 auto;
}
</style>
