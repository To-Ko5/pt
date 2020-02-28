<template>
  <div class="container">
    <h2>Skill</h2>
    <section class="skill-area">
      <div class="slill-area-left">
        <h3 class="skill-title">FRONT END</h3>
        <ul class="skill-list">
          <li>
            <img class="skill-img" src="~/assets/skill_img/html-5.svg" alt="HTML5" />HTML
          </li>
          <li>
            <img class="skill-img" src="~/assets/skill_img/css-3.svg" alt="CSS3" />CSS
          </li>
          <li>
            <img class="skill-img" src="~/assets/skill_img/javascript.svg" alt="JavaScript" />JavaScript
          </li>
          <li>
            <img class="skill-img" src="~/assets/skill_img/vue.svg" alt="Vue.js" />Vue.js
          </li>
          <li>
            <img class="skill-img" src="~/assets/skill_img/nuxt.svg" alt="Vue.js" />Nuxt.js
          </li>
        </ul>
      </div>
      <div class="slill-area-center">
        <h3 class="skill-title">BACK END</h3>
        <ul class="skill-list">
          <li>
            <img class="skill-img" src="~/assets/skill_img/php.svg" alt="PHP" />PHP
          </li>
          <li>
            <img class="skill-img" src="~/assets/skill_img/mysql.svg" alt="MySQL" />MySQL
          </li>
        </ul>
        <h3 class="skill-title">DEVELOPMENT TOOLS</h3>
        <ul class="skill-list">
          <li>
            <img class="skill-img" src="~/assets/skill_img/git.svg" alt="Git" />Git
          </li>
          <li>
            <img class="skill-img" src="~/assets/skill_img/github.svg" alt="Github" />Github
          </li>
        </ul>
      </div>
      <div class="slill-area-left">
        <h3 class="skill-title">DESIGN TOOLS</h3>
        <ul class="skill-list">
          <li>
            <img class="skill-img" src="~/assets/skill_img/photoshop.svg" alt="photoshop" />Photoshop
          </li>
          <li>
            <img class="skill-img" src="~/assets/skill_img/illustrator.svg" alt="Illustrator" />Illustrator
          </li>
        </ul>
      </div>
    </section>
  </div>
</template>


<style lang="scss" scoped>
.skill-area {
  display: flex;
  justify-content: space-between;
  .skill-title {
    font-size: 2rem;
    width: 100%;
    margin-bottom: 30px;
    background: #333;
    color: #fff;
    padding: 8px;
  }
  .skill-list {
    & li {
      line-height: 1.6;
      height: 1.6;
      font-size: 1.6rem;
      vertical-align: center;
      .skill-img {
        width: 50px;
        vertical-align: middle;
        margin-right: 10px;
      }
    }
    & li:not(:last-of-type) {
      margin-bottom: 20px;
    }
    &:nth-of-type(1) {
      margin-bottom: 50px;
    }
  }
}

.slill-area-left,
.slill-area-center,
.slill-area-left {
  width: 30%;
}

@media screen and (max-width: 700px) {
  .skill-area {
    display: block;
    .skill-title {
      margin-bottom: 20px;
    }
    .skill-list {
      & li:not(:last-of-type) {
        margin-bottom: 24px;
      }
      &:nth-of-type(1) {
        margin-bottom: 24px;
      }
    }
    .skill-list:nth-of-type(2) {
      margin-bottom: 24px;
    }
  }
  .slill-area-left,
  .slill-area-center,
  .slill-area-left {
    width: 100%;
  }
}
</style>