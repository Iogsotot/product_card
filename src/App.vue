<template>
  <div id="app">

    <div class="flex">
      <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
      <Header class="header"/>
      
      <main>
        <ProductTitle class="product_title container"/>

        <section class="wrapper flex container">      
          <PictureField class="picture_field"/>
          <ProductInfo class="product_info"/>
        </section>

        <Tabs class="tabs-block"/>
        <PopupBuyForm class="popup_buy_form hidden"/>
      </main>
      <Footer class="footer"/>
    </div>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Header from './components/Header.vue'
import ProductTitle from './components/ProductTitle.vue'
import PictureField from './components/PictureField.vue'
import ProductInfo from './components/ProductInfo.vue'
import Tabs from './components/Tabs.vue'
import PopupBuyForm from './components/PopupBuyForm.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'app',
  components: {
    // HelloWorld,
    ProductTitle,
    Header,
    PictureField,
    ProductInfo,
    Tabs,
    PopupBuyForm,
    Footer
  }
}

</script>

<style>
#app {
  font-family: 'Pt Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

html {
  font-size: 14px;
  font-family: 'Pt Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif;
  color: #333;
  direction: ltr;
  box-sizing: border-box;
  }

* {
  padding: 0;
  margin: 0;
}

li {
  list-style: none;
}

a, a:active {
  text-decoration: none;
  color: #333;
}

.flex {
  display: flex;
  flex-wrap: nowrap;
  flex-direction: column;
  justify-content: center; 
}

.container {
  padding: 0 calc(50% - 590px);
}

.product_title {
  margin: 1rem;
}

.wrapper {
  flex-direction: row;
  justify-content: center; 
  max-width: 100vw;
  text-align: left;  
}

.picture_field {
  min-height: 60vh;
  width: 65%;
  margin: 0 1rem;
}

.product_info {
  max-width: 45%;
}

.tabs-block {
    margin: 1rem 0;
    background-color: rgb(214, 240, 238, .8);
    padding: 0;
}

.hidden {
  display: none;
}

</style>
