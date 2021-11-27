<template>
  <div class="banner">
    <div class="banner-wrap" v-for="item in bannerData">
      <div class="image" :style="{order: item.order}">
        <img :src="require('@/assets/media/' + item.imageBanner)" alt="">
      </div>
      <div class="text">
        <h1 class="title">{{item.title}}</h1>
        <p class="paragraph">{{item.paragraph}}.</p>
        <button>Learn More</button>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "banner",

  data() {
    return {
      bannerData: [
      {
        imageBanner: 'honey&flower.png',
        title: 'Honey created in the laps of nature.',
        paragraph: 'Honey is one of the prime ingredients in your everyday food schedule. As a brand, you need a marketing strategy that will help...',
        order: 0,
      },
      {
        imageBanner: 'beehouse2.png',
        title: 'Does your honey taste bad? Try us!',
        paragraph: 'Honey is one of the prime ingredients in your everyday food schedule. As a brand, you need a marketing strategy that will help...',
        order: 1,
      },
    ]
    }

  }
}
</script>

<style lang="scss" scoped>


.banner {
  width: 100%;
  padding: 0 3.668vw;
}

.banner-wrap {
  width: 100%;
  height: 52.444vw;
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 8.028vw 0;
  &:first-child{
    margin-right: 4vw;
  }
  &:nth-child(2){
    margin-left: 3vw;
  }
  .image {
    width: 55.639vw;
    height: 100%;
    img {
      width: 100%;
      height: 100%;
      object-fit: contain;
    }
  }

  .text {
    width: 35.833vw;

    h1 {
      font-size: 3.125vw;
      margin-bottom: 2.083vw;
      font-family: 'Kochasan Bold', sans-serif;
    }

    p {
      font-size: 1.528vw;
      line-height: 2.431vw;
    }

    button {
      margin-top: 3.472vw;
      width: 12.778vw;
      background: #FF9D2D;
      color: white;
      height: 4.097vw;
      outline: none;
      border: none;
      font-size: 1.250vw;
      cursor: pointer;
    }
  }

}
</style>