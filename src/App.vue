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

        <Tabs/>
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
  font-family: 'Pt Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif;
  color: #333;
  direction: ltr;
  box-sizing: border-box;
  }

h1, h2, h3 {
  font-family: 'Montserrat', sans-serif;
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

.product_title {
  margin: 1rem;
}

.wrapper {
  flex-direction: row;
  justify-content: center; 
  max-width: 100vw;
  text-align: left;  
}

/* .picture_field {
  min-height: 60vh;
  width: 65%;
  margin: 0 1rem;
}

.product_info {
  max-width: 45%;
  padding-left: 1rem;
} */

  .picture_field {
    min-height: 50vh;
    width: 65%;
    margin: 0 1rem;
}

  .product_info {
    max-width: 35%;
    padding-left: 1rem;
  }

.hidden {
  display: none;
}

.container {
  padding: 0 15px;
  max-width: unset !important;
  margin: unset !important;
}

@media (max-width: 576px) {
   html {
    font-size: 12px;
  }
    .container {
    padding: 0 calc(50vw - 270px);
    max-width: unset !important;
    margin: unset !important;
  }

}

@media (min-width: 575.98px){
  html {
    font-size: 12px;
  }
  .container {
    padding: 0 calc(50vw - 260px);
    max-width: unset !important;
    margin: unset !important;
  }

}

@media (min-width: 767.98px){
  html {
    font-size: 14px;
  }

  .container {
    padding: 0 calc(50vw - 370px)!important;
    max-width: unset !important;
    margin: unset !important;
  }

  .picture_field {
  min-height: 60vh;
  width: 65%;
}

  .product_info {
    max-width: 45%;
  }
}

@media (min-width: 991.98px) {
 
  .container {
    padding: 0 calc(50vw - 480px)!important;
    max-width: unset !important;
    margin: unset !important;
  }
}

@media (min-width: 1199.98px){
  html {
    font-size: 16px;
  }
  .container {
    padding: 0 calc(50vw - 590px)!important;
    max-width: unset !important;
    margin: unset !important;
  }
}


</style>
