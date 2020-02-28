<template>
  <div class="container">
    <h2>About</h2>
    <div class="about-content-area">
      <p>前職では、ビルの設備管理の仕事をしておりました。</p>
      <p></p>
      <p>その後、職業訓練のWebサイト制作科に通い、HTML・CSS・JavaScript・PHP・MYSQL等を学びました。現在はSES企業に勤務しています。</p>
      <p>Vue.js、Nuxt.js等を学習中で、フロントエンドの分野に携わりたいと考えています。</p>
      <p>こちらのポートフォリオサイトもNuxt.jsで作成しています。</p>
    </div>
    <div class="about-area-flex">
      <ul class="link-list">
        <li>
          <a href="https://github.com/To-Ko5" target="_blank">
            <img class="skill-img" src="~/assets/skill_img/github.svg" alt="Github" />GitHub
          </a>
        </li>
        <li>
          <a href="https://qiita.com/To-K" target="_blank">
            <img class="skill-img" src="~/assets/skill_img/qiita.png" alt="Qiita" />Qiita
          </a>
        </li>
      </ul>

      <section class="license">
        <h3 class="license-title">保有資格</h3>
        <ul class="license-list">
          <li>第二種電気工事士</li>
          <li>乙種第４類危険物取扱者</li>
          <li>一級ボイラー技士</li>
          <li>消防設備士甲種 4類</li>
          <li>建築物環境衛生管理技術者</li>
          <li>PHP7技術者認定初級試験</li>
        </ul>
      </section>
    </div>
  </div>
</template>


<style lang="scss" scoped>
.about-content-area {
  margin-bottom: 70px;
  & p {
    line-height: 1.7;
  }
}

.about-area-flex {
  display: flex;
  justify-content: space-around;
}

.link-list {
  & li {
    vertical-align: center;
    & a {
      text-decoration: underline;
      font-size: 2rem;
    }
    .skill-img {
      width: 50px;
      vertical-align: middle;
      margin-right: 10px;
    }
  }
  & li:first-of-type {
    margin-bottom: 40px;
  }
}

.license {
  .license-title {
    margin-bottom: 20px;
    font-size: 2rem;
  }
  ul {
    list-style-type: square;
    margin-left: 20px;
    & li {
      line-height: 1.7;
    }
  }
}

@media screen and (max-width: 768px) {
  .about-content-area {
    margin-bottom: 20px;
  }
  .about-area-flex {
    display: block;
  }

  .link-list {
    margin-bottom: 40px;
    & li {
      & a {
        font-size: 1.6rem;
      }
    }
    & li:first-of-type {
      margin-bottom: 20px;
    }
  }
}
</style>