<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <div class="grid">
      <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
      <Header class="header"/>
      <ProductTitle class="product_title" msg="Название товара"/>
      <PictureField class="picture_field"/>
      <ProductInfo class="product_info"/>
      <Tabs class="tabs"/>
      <PopupBuyForm class="popup_buy_form"/>
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
  font-size: 12px;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #333;;
}

.grid {
  display: grid;
  grid-template-columns: 2fr 1fr;
  grid-template-rows: 1.5fr 1fr 4fr 1fr 1fr;

  margin: 1.5rem;
  margin-top: 4.5rem;
}

.header {
  grid-row: 1/2;
  grid-column: 1/3;
}

.product_title {
  grid-row: 2/3;
  grid-column: 1/3;
}

.picture_field {
  grid-row: 3/4;
  grid-column: 1/2;
}

.product_info {
  grid-row: 3/4;
  grid-column: 2/3;
}

.tabs {
  grid-row: 4/5;
  grid-column: 1/3;
}

.popup_buy_form {
  display: none;
  grid-row: 1/2;
  grid-column: 1/3;
}

.footer {
  grid-row: 5/6;
  grid-column: 1/3;
}

</style>
