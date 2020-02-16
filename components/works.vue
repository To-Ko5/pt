<template>
  <div class="container">
    <h2>Works</h2>
    <div class="works-area">
      <div class="web-area">
        <p class="work-img">
          <img src="~/assets/web/webdesign01.jpg" alt="webdesign01" />
        </p>
        <p class="work-img">
          <img src="~/assets/web/webdesign02.jpg" alt="webdesign02" />
        </p>
        <p class="work-img">
          <img src="~/assets/web/taskmanagement.jpg" alt="taskmanagement" />
        </p>
      </div>
      <div class="banner-area">
        <p class="work-img">
          <img src="~/assets/banner/fashion-w-banner.jpg" alt="banner1" />
        </p>
        <p class="work-img">
          <img src="~/assets/banner/fashion-m-banner.jpg" alt="banner2" />
        </p>
        <p class="work-img">
          <img src="~/assets/banner/fitness.jpg" alt="banner3" />
        </p>
      </div>
    </div>
    <p class="view-more-btn-outer">
      <nuxt-link to="/works/#works" class="view-more-btn">view more</nuxt-link>
    </p>
  </div>
</template>


<style lang="scss" scoped>
@import "assets/style/btn.scss";

.web-area,
.banner-area {
  display: flex;
  justify-content: space-between;
}

.web-area {
  margin-bottom: 30px;
}

.banner-area {
  margin-bottom: 60px;
}

.work-img {
  width: 30%;
  & img {
    box-shadow: 1px 1px 3px #333;
  }
}

@media screen and (max-width: 768px) {
  .web-area,
  .banner-area {
    display: block;
  }

  .web-area {
    margin-bottom: 20px;
  }

  .banner-area {
    margin-bottom: 30px;
  }

  .work-img {
    width: 100%;
    margin-bottom: 10px;
    text-align: center;
  }

  .view-more-btn-outer {
    width: 220px;
  }
}
</style>