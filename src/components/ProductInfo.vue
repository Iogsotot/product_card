<template>
  <article>
    <h1 class="price">{{price}} <span class="price-r"> &#8381; </span> </h1>
    <div class="rating">{{rating}}</div>
    <button>Купить в 1 клик</button>
  
    <div class="in_stock" v-on:click="show = !show">Наличие</div>
    <transition name="fade">
      <p v-if="show">более 10 шт. на складе</p>
    </transition>

    <ul class="shipment">
      <li class="shipment_city"><b>Санкт-Петербург.</b> <a href="#">Выбрать город доставки</a></li>
      <li class="delivery">Доставка - c 24 Ноября (265&#8381;)</li>
      <li class="pickup">Самовывоз - c 22 Ноября (БЕСПЛАТНО)</li>
    </ul>
  </article>
</template>

<script>
export default {
  name: 'ProductInfo',
  data() {
    return { 
      price: '5 785',
      rating: '100%',
      show: false
      }
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .price {
    font-size: 3rem;
    font-weight: bold;
  }

  .price-r {
    font-size: 2.4rem;
  }

  .in_stock {
    position: relative;
    width: 5rem;

    margin-top: 4rem;

    font-size: 1rem;
    font-weight: 100;
    color: rgb(0, 128, 0);

    border-bottom: 1px dashed #008000;

    cursor: pointer;
  }

  .in_stock::after {
    content: '';
    position: absolute;
    top: 50%;
    right: 0;
    margin-top: -4px;

    width: 8px;
    height: 8px;
    border-right: 2px solid green;
    border-bottom: 2px solid green;
    border-radius: 2px;
    transform: rotate(45deg);
  }

  .fade-enter-active {
  transition: all .3s ease;
  }
  .fade-leave-active {
    transition: all .6s cubic-bezier(1.0, 0.5, 0.8, 1.0);
  }
  .fade-enter {
    transform: translateY(-10px);
    opacity: 0;
  }

  .fade-leave-to {
    transform: translateX(10px);
    opacity: 0;
  }

  .shipment {
    font-weight: 100;
    color: #727272;
  }

  .shipment_city {
    margin: 1rem 0 .4rem;
  }

  .shipment_city > a {
    text-decoration: underline;
    color: #727272;
  }

  .shipment_city > b {
    font-weight: bold;
    color: #333;
  }

  /* .hidden {
  display: none;
} */



</style>

