<template>
  <div class="products-container">
    <div class="titles-wrapper">
      <h1>Our products</h1>
      <a href="/" class="products-link">See all</a>
    </div>
    <div class="products-wrapper">

      <div class="product" v-for="item in productsData">
        <div class="text">
          <h1>{{ item.name }}</h1>
          <p>{{ item.paragraph }}</p>
          <button>Buy Now</button>
        </div>
        <div class="image">
          <img :src="require('@/assets/media/' + item.image)" alt="">
        </div>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: "products",
  data() {
    return {
      productsData: [
        {
          name: 'Eucalyptus Honey',
          paragraph: 'It has the scent of lavender, medium sweetness lavender scented, and has a medium amber color.',
          image: 'honeymug.png'
        },
        {
          name: 'Basswood Honey',
          paragraph: 'Basswood is a tree native and abundant in Wisconsin, which is also known as the Linden tree.',
          image: 'honeyinglass.png'
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>

.titles-wrapper {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 3.472vw;
  @media(max-width: 433px) {

  }

  h1 {
    font-size: 3.125vw;
    @media(max-width: 433px) {
      font-size: 10.125vw;
    }
  }

  a {
    color: #FF9D2D;
    font-weight: 600;
    transform: translateY(0.8vw);
    font-size: 1.250vw;
    @media(max-width: 433px) {
      font-size: 4.25vw;
    }
  }
}

.products-container {
  width: 79.583vw;
  margin: 0 auto;
  display: flex;
  justify-content: center;
  flex-direction: column;
  @media(max-width: 433px) {
    width: 93.583vw;
    margin-top: 36vw;
  }
}

.products-wrapper {
  display: flex;
  align-items: center;
  justify-content: space-between;
  @media(max-width: 433px) {
    flex-direction: column;
  }
}

.product {
  padding: 3.125vw 2.083vw;
  width: 38.750vw;
  height: 21.181vw;
  background: #FDF6EE;
  display: flex;
  align-items: flex-start;
  justify-content: flex-start;
  position: relative;
  @media(max-width: 433px) {
    width: 91.75vw;
    height: 42.181vw;
    margin-top: 9vw;
    margin-bottom: 7vw;
  }

  .text {
    width: 20.972vw;
    @media(max-width: 433px) {
      width: 64.972vw;

    }

    h1 {
      font-size: 1.944vw;
      @media(max-width: 433px) {
        font-size: 6.944vw;
      }
    }

    p {
      padding: 1.875vw 0;
      font-size: 1.111vw;
      font-family: 'Kochasan Semibold', sans-serif;
      line-height: 2.000vw;
      @media(max-width: 433px) {
        font-size: 3.111vw;
        line-height: 4vw;
      }
    }

    button {
      border: 0.208vw solid #FF9D2D;
      color: #FF9D2D;
      background: transparent;
      outline: none;
      width: 9.722vw;
      height: 3.403vw;
      font-size: 1.250vw;
      @media(max-width: 433px) {
        width: 23.722vw;
        height: 10.403vw;
        font-size: 4.25vw;
      }
    }
  }

  .image {
    width: 16.250vw;
    height: 15.222vw;
    position: absolute;
    top: 50%;
    right: 0;
    transform: translateY(-50%);
    @media(max-width: 433px) {
      width: 33.25vw;
      height: 35.222vw;
    }

    img {
      width: 100%;
      height: 100%;
      object-fit: contain;
      @media(max-width: 433px) {

      }
    }
  }
}

</style>