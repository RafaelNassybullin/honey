<template>
  <div class="banner">
    <div class="banner-wrap" v-for="item in bannerData">
      <div class="image" :style="{order: item.order}">
        <img :src="require('@/assets/media/' + item.imageBanner)" alt="">
      </div>
      <div class="text">
        <h1 class="title">{{ item.title }}</h1>
        <p class="paragraph">{{ item.paragraph }}.</p>
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
  @media(max-width: 433px) {
    height: 415vw;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-direction: column;
  }
}

.banner-wrap {
  width: 100%;
  height: 52.444vw;
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 8.028vw 0;
  @media(max-width: 433px) {
    height: 139.444vw;
    margin: 30.028vw 0;
    flex-direction: column;
  }
  &:first-child {
    margin-right: 4vw;
    @media(max-width: 433px) {
      margin-right: 0;
    }
  }
  &:nth-child(2) {
    margin-left: 3vw;
    .image {
      @media(max-width: 433px) {
        order: -1;
      }
    }
    @media(max-width: 433px) {
      margin-left: 0;
      margin-top: 9vw;
    }
  }
  .image {
    width: 55.639vw;
    height: 100%;
    @media(max-width: 433px) {
      width: 97.639vw;
    }

    img {
      width: 100%;
      height: 100%;
      object-fit: contain;
    }
  }

  .text {
    width: 35.833vw;
    @media(max-width: 433px) {
      width: 96.833vw;
    }

    h1 {
      font-size: 3.125vw;
      margin-bottom: 2.083vw;
      font-family: 'Kochasan Bold', sans-serif;
      @media(max-width: 433px) {
        font-size: 8.125vw;
        margin-bottom: 7.083vw;
      }
    }

    p {
      font-size: 1.528vw;
      line-height: 2.431vw;
      @media(max-width: 433px) {
        font-size: 4.528vw;
        line-height: 5.431vw;
      }
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
      @media(max-width: 433px) {
        width: 42.778vw;
        height: 13.097vw;
        font-size: 5.25vw;
      }
    }
  }

}
</style>