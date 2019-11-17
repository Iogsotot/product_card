<template>
  <div>
    <h1 class="price">
      {{price}}
      <span class="price-r">&#8381;</span>
    </h1>
    <div>
      <img :src="rating" alt class="rating" />
    </div>

    <div class="in_stock_group">
      <div class="in_stock" v-on:click="show = !show">Наличие</div>
      <transition name="fade">
        <p v-if="show">более 10 шт. на складе</p>
      </transition>
    </div>

    <ul class="shipment">
      <li class="shipment_city">
        <b>Санкт-Петербург.</b>
        <a href="#">Выбрать город доставки</a>
      </li>
      <li class="delivery">Доставка - c 24 Ноября (265&#8381;)</li>
      <li class="pickup">Самовывоз - c 22 Ноября (БЕСПЛАТНО)</li>
    </ul>

    <b-button class="buy-btn" @click="modalShow = !modalShow">Закажите сейчас</b-button>
    <div class="form">
      <b-modal
        v-model="modalShow"
        ok-title="отправить заказ"
        cancel-title="сбросить"
        title="Заказать"
        @ok="submit"
        @cancel="reset"
      >
        <b-form>
          <b-form-group
            id="input-group-1"
            label="Ваш телефон:"
            label-for="input-1"
            description="Мы не раскрываем Ваши данные третьим лицам."
          >
            <b-form-input
              id="input-1"
              v-model="form.phone"
              type="tel"
              required
              placeholder="Введите телефон"
            ></b-form-input>
          </b-form-group>

          <b-form-group id="input-group-2" label="Ваше имя:" label-for="input-2">
            <b-form-input id="input-2" v-model="form.name" required placeholder="Введите имя"></b-form-input>
          </b-form-group>
        </b-form>
      </b-modal>
    </div>

    <div class="vet-control">
      <img src="./../assets/imgs/vet_icon.png" width="70" alt />
      <div>Все животные имеют ветеринарные сертификаты</div>
    </div>
  </div>
</template>

<script>
import rating_icon from "./../assets/imgs/rating_icon_gold.png";

export default {
  name: "ProductInfo",
  data() {
    return {
      price: "95 785",
      // rating: "100%",
      rating: rating_icon,
      show: false,
      modalShow: false,
      form: {
        phone: "",
        name: ""
      }
    };
  },
  props: {
    msg: String
  },
  methods: {
    submit() {
      var formData = JSON.stringify(this.form);

      alert(formData);
    },
    reset(evt) {
      evt.preventDefault();
      // Сбрасываем значения формы
      this.form.phone = "";
      this.form.name = "";
    }
  }
};
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

/* popup (start) */
.buy-btn {
  display: initial;

  font-size: 1.2rem;
  font-weight: 700;
  background: #00a651 !important;
  color: #fff;
  border: 1px solid transparent !important;

  text-decoration: none;
  user-select: none;

  padding: 0.8rem 1.2rem;
  margin: 2rem auto 2rem;

  outline: none;
}

.buy-btn:hover {
  cursor: pointer;
  background: #fff !important;
  color: #00a651 !important;
  transition: 0.3s;
  border-color: #00a651 !important;
}

.buy-btn:active {
  top: 1px;
  color: #fff;
}

/* popup (end) */

/* collapse (start) */
.in_stock_group {
  height: 2.5rem;
}

.in_stock {
  position: relative;
  width: 5rem;

  margin-top: 1rem;

  font-size: 1rem;
  font-weight: 100;
  color: rgb(0, 128, 0);

  border-bottom: 1px dashed #008000;

  cursor: pointer;
}

.in_stock::after {
  content: "";
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
  transition: all 0.3s ease;
}
.fade-leave-active {
  transition: all 0.6s cubic-bezier(1, 0.5, 0.8, 1);
}
.fade-enter {
  transform: translateY(-10px);
  opacity: 0;
}

.fade-leave-to {
  transform: translateX(10px);
  opacity: 0;
}
/* collapse (end) */

.rating {
  width: 100px;
}

.shipment {
  font-weight: 100;
  color: #727272;
}

.shipment_city {
  margin: 0.4rem 0 0.4rem;
}

.shipment_city > a {
  text-decoration: underline;
  color: #727272;
}

.shipment_city > b {
  font-weight: bold;
  color: #333;
}

.vet-control {
  display: flex;
  justify-content: center;
  margin: 1rem 0 1rem;
  font-weight: bold;
}

.vet-control img {
  height: 46.55px;
  width: 70px;
  display: inline-block;
  margin-right: 0.5rem;
}

@media (max-width: 605px) {
  .vet-control div {
    display: none;
  }
  .vet-control img {
    margin-right: 0;
  }

  .buy-btn {
    display: block;
    margin: 2.5rem auto 1.5rem;
  }
}

@media (max-width: 490px) {
  .price {
    font-size: 2.5rem;
  }

  .price-r {
    font-size: 2rem;
  }
}

@media (max-width: 460px) {
  .buy-btn {
    padding: 1rem;
  }
}

@media (max-width: 440px) {
  .buy-btn {
    padding: 0.6rem;
  }
}
</style>

<style>
button.btn.btn-primary {
  background: #00a651;
  color: #fff;
  border: 1px solid transparent;
  margin-left: 1.5rem;
}

button.btn.btn-primary:hover {
  background: #fff;
  color: #00a651;
  border-color: #00a651;
  transition: 0.3s;
}

button.btn.btn-primary:active,
.btn-primary:not(:disabled):not(.disabled):active,
.btn-primary:not(:disabled):not(.disabled).active,
.show > .btn-primary.dropdown-toggle {
  background: #01d837 !important;
  border-color: #00a651 !important;
  color: #fff;
  transition: 0.3s;
}

button.btn.btn-secondary {
  background: #395346;
  color: #fff;
  border: 1px solid transparent;
}

button.btn.btn-secondary:hover {
  background: #fff;
  color: #395346;
  border-color: #395346;
  transition: 0.3s;
}
</style>

