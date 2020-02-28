<template>
  <LightBox ref="lightbox" :images="images" :show-light-box="false" :show-thumbs="false"></LightBox>
</template>

<script>
export default {
  data() {
    return {
      images: [
        { src: FashionM },
        { src: FashionW },
        { src: Fitness },
        { src: Businessdepartment },
        { src: Thai },
        { src: TensyokuMikeiken },
        { src: Sakura },
        { src: Shinryoku },
        { src: Koyo },
        { src: Yukigeshiki },
        { src: RainyBanner },
        { src: SeminarBanner },
        { src: Shoes1 },
        { src: Shoes2 },
        { src: Seitai }
      ]
    };
  },
  methods: {
    showBanner(index) {
      this.$refs.lightbox.showImage(index);
    }
  }
};
</script>