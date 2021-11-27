<template>

  <nav>
    <navigation/>
  </nav>


  <main>
    <hero/>
  </main>


  <section>
    <shops/>
  </section>


  <section>
    <banner/>
  </section>


  <section>
    <products/>
  </section>


  <footer>
    <footerr/>
  </footer>


</template>
<script>

import navigation from './components/navigation'
import hero from './components/hero'
import shops from './components/shops'
import banner from './components/banner'
import products from './components/products'
import footerr from './components/footerr'
import './assets/font/fonts.css'


export default {
  components: {
    navigation,
    hero,
    shops,
    banner,
    products,
    footerr
  }
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Kochasan Regular', sans-serif;
}

nav {
  width: 100%;
  height: 6.944vw;
  padding: 0 3.472vw;
  display: flex;
  align-items: center;
  justify-content: flex-end;
}

main {
  padding: 0 3.472vw;
  margin-bottom: 9.028vw;
}

</style>
