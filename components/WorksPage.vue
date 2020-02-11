<template>
    <div class="container">
        <h2>Works</h2>
        <div class="works-area">
            <div class="works-content" @click="show('Eternity')">
                <div class="img-effect">
                    <img src="~/assets/web/webdesign01.jpg" alt="webdesign01">
                </div>
            </div>

            <div class="works-content" @click="show('Suslon')">
                <div class="img-effect">
                    <img src="~/assets/web/webdesign02.jpg" alt="webdesign02">
                </div>
            </div>

            <div class="works-content" @click="show('Nemesis')">
                <div class="img-effect">
                    <img src="~/assets/web/webdesign03.jpg" alt="webdesign03">
                </div>
            </div>

            <div class="works-content" @click="show('Masquerade')">
                <div class="img-effect">
                    <img src="~/assets/web/webdesign04.jpg" alt="webdesign04">
                </div>
            </div>

            <div class="works-content" @click="show('BuildingMaintenance')">
                <div class="img-effect">
                    <img src="~/assets/web/webdesign05.jpg" alt="webdesign05">
                </div>
            </div>

            <div class="works-content" @click="show('PictureOfLight')">
                <div class="img-effect">
                    <img src="~/assets/web/webdesign07.jpg" alt="webdesign07">
                </div>
            </div>
            
            <div class="works-content" @click="show('TaskManagementApp')">
                <div class="img-effect">
                    <img src="~/assets/web/taskmanagement.jpg" alt="taskmanagement">
                </div>
            </div>

            <div class="works-content" @click="show('EasyMemo')">
                <div class="img-effect">
                    <img src="~/assets/web/programming01.jpg" alt="EasyMemo">
                </div>
            </div> 

            <div class="works-content" @click="show('SimpleBulletinBoard')">
                <div class="img-effect">
                    <img src="~/assets/web/Simplebulletinboard.jpg" alt="SimpleBulletinBoard">
                </div>
            </div>
            
            <div v-for="(img,index) in bannerImages" :key="index" class="works-content" @click="showBanner(index)">
                <img :src="`${img}`">
            </div>                                      
            
        </div>
        
        <client-only>
          <modal name="modal-content"  width="80%" height="auto" :scrollable="true">
            <p class="close-btn" @click="hide"><i class="fas fa-times"></i></p>
            <component :is="contentTitle"/>
          </modal>
          <LightBox ref="lightbox" :images="images" :show-light-box="false" :show-thumbs="false"></LightBox>
        </client-only>
    </div>
</template>
​
​
<script>
import Eternity from '~/components/works/Eternity.vue'
import Suslon from '~/components/works/Suslon.vue'
import Nemesis from '~/components/works/Nemesis.vue'
import Masquerade from '~/components/works/Masquerade.vue'
import BuildingMaintenance from '~/components/works/BuildingMaintenance.vue'
import Zephyr from '~/components/works/Zephyr.vue'
import PictureOfLight from '~/components/works/PictureOfLight.vue'
import TaskManagementApp from '~/components/works/TaskManagementApp.vue'
import EasyMemo from '~/components/works/EasyMemo.vue'
import SimpleBulletinBoard from '~/components/works/SimpleBulletinBoard.vue'

import FashionM from '~/assets/banner/fashion-m-banner.jpg'
import FashionW from '~/assets/banner/fashion-w-banner.jpg'
import Fitness from '~/assets/banner/fitness.jpg'
import Businessdepartment from '~/assets/banner/businessdepartment-banner.jpg'
import Thai from '~/assets/banner/thai-banner.jpg'
import TensyokuMikeiken from '~/assets/banner/tensyoku-mikeiken-banner.jpg'
import Sakura from '~/assets/banner/sakura-banner.jpg'
import Shinryoku from '~/assets/banner/shinryoku-banner.jpg'
import Koyo from '~/assets/banner/koyo-banner.jpg'
import Yukigeshiki from '~/assets/banner/yukigeshiki-banner.jpg'
import Shoes1 from '~/assets/banner/shoes1.jpg'
import Shoes2 from '~/assets/banner/shoes2.jpg'
import SeminarBanner from '~/assets/banner/seminar-banner.jpg'
import RainyBanner from '~/assets/banner/rainy-banner.jpg'
import Seitai from '~/assets/banner/seitai2.jpg'

import LightBox from 'vue-image-lightbox'
require('vue-image-lightbox/dist/vue-image-lightbox.min.css')


export default {
    data(){
      return {
        contentTitle: null,
        bannerImages: [
            FashionM,FashionW,Fitness,Businessdepartment,Thai,TensyokuMikeiken,Sakura,Shinryoku,Koyo,Yukigeshiki,RainyBanner,SeminarBanner,Shoes1,Shoes2,Seitai
        ],
        images: [
            {src: FashionM},{src: FashionW},{src: Fitness},{src: Businessdepartment},{src: Thai},{src: TensyokuMikeiken},{src: Sakura},{src: Shinryoku},{src: Koyo},{src: Yukigeshiki},{src: RainyBanner},{src: SeminarBanner},{src: Shoes1},{src: Shoes2},{src: Seitai}
        ],
      }
    },
    components: {
      Eternity,Suslon,Nemesis,Masquerade,BuildingMaintenance,PictureOfLight,TaskManagementApp,EasyMemo,SimpleBulletinBoard,LightBox
    },
    methods: {
        show (contentTitle) {
          this.contentTitle = contentTitle
          this.$modal.show("modal-content");
        },
        hide (contentTitle) {
          this.$modal.hide("modal-content");
          this.contentTitle = null
        },
        showBanner(index){
          this.$refs.lightbox.showImage(index)
        }
    }
}
</script>

<style lang="scss" scoped>

.works-area {
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    margin-bottom: 30px;
    .works-content {
        width: 300px;
        box-shadow: 1px 1px 3px #333;
        overflow: hidden;
        margin-bottom: 30px;
        cursor: pointer;
        .img-effect {
            position: relative;
            width: 300px;
            height: 180px;
            transition-duration: 0.3s;
            &:hover {
                transform: scale(1.1);
                &:before {
                    opacity: 1;
                    transform: scale(1.2);
                    filter: blur(0);
                }
            }
            &:before {
                content: "view more";
                position: absolute;
                width: 300px;
                height: 180px;
                background: radial-gradient(rgba(0, 0, 0, 0.2), rgba(0, 0, 0, 0.8)); 
                transition-duration: 0.3s;
                opacity: 0; 
                display: flex; 
                justify-content: center; 
                align-items: center;
                color: #fff;
                font-size: 22px;
                text-shadow: 0 0 2px #000;
                filter: blur(4px); /* ブラー効果 */
            }
        }
    }
}

.close-btn {
    width: 50px;
    height: 50px;
    line-height: 50px;
    font-size: 3rem;
    color: #fff;
    text-align: center;
    background: #333;
    cursor: pointer;
}

@media screen and (max-width: 768px) {
  .works-area {
    margin-bottom: 0;
  }
}
</style>