<template>
    <div class="container">
        <h2>skill</h2>
        <div class="skill-area">
            <div class="skill-content">
                <p class="skill-image"><img src="~/assets/skill_img/01.svg"></p>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco</p>
            </div>
            <div class="skill-content">
                <p class="skill-image"><img src="~/assets/skill_img/02.svg"></p>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. </p>
            </div>
            <div class="skill-content">
                <p class="skill-image"><img src="~/assets/skill_img/03.svg"></p>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor</p>
            </div>
            <div class="skill-content">
                <p class="skill-image"><img src="~/assets/skill_img/04.svg"></p>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut</p>
            </div>
            <div class="skill-content">
                <p class="skill-image"><img src="~/assets/skill_img/05.svg"></p>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad </p>
            </div>
            <div class="skill-content">
                <p class="skill-image"><img src="~/assets/skill_img/06.svg"></p>
                <p> sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua</p>
            </div>
        </div>
    </div>    
</template>


<script>
export default {
    data(){
        return {
            imgList: ['01','02','03','04'],
            
        }
    }
}
</script>

<style lang="scss">
h2 {
    text-align: center;
    margin-bottom: 20px;
}

.skill-area {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    background: rgba(34, 26, 26, 0.144);
    .skill-content {
        width: 30%;
        padding: 20px;
        box-sizing: border-box;
        margin-bottom: 20px;
        .skill-image{
            margin-bottom: 20px;
            & img {
                display: block;
                height: 200px;
                width: 200px;
                margin: auto;
                // opacity: 0.4;
             }
        }
    }
}
</style>