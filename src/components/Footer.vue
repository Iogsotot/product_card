<template>
  <footer>
    <div class="container page-footer">    
      <div class="footer-middle">
        <div class="footer-menu">
          <h3>Магазин</h3>
          <ul>
            <li>
              <a href="#">Для котиков</a>
            </li>
            <li>
              <a href="#">Для собачек</a>
            </li>
            <li>
              <a href="#">Для птичек</a>
            </li>
            <li>
              <a href="#">Для рептилий</a>
            </li>
          </ul>
        </div>

        <div class="footer-menu">
          <h3>Отзывы</h3>
          <ul>
            <li>
              <a href="#">Показать</a>
            </li>
            <li>
              <a href="#">Оставить</a>
            </li>
          </ul>
        </div>

        <div class="footer-menu">
          <h3>Прайс-лист</h3>
          <ul>
            <li>
              <a href="#">Скачать прайс</a>
            </li>
          </ul>
        </div>
      </div>
      <div class="footer-bottom">
        <div class="footer-social">
          <b>Мы в соц. сетях:</b>
          <a href="#" class="social-btn social-btn-vk">
            <span class="sr-only">Вконтакте</span>
          </a>
          <a href="#" class="social-btn social-btn-fb">
            <span class="sr-only">Фейсбук</span>
          </a>
          <a href="#" class="social-btn social-btn-in">
            <span class="sr-only">Инстаграм</span>
          </a>
        </div>
        <div class="footer-copyright">
          С
          <span class="heart">
            <span class="sr-only">любовью</span>
          </span> для
          <a href="#">каждого существа</a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",

  props: {
    msg: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
footer {
  display: flex;
  flex-direction: column;
  flex-wrap: nowrap;
  justify-content: center;
  background-color: rgba(223, 230, 243, 0.664);
}

.page-footer {
  padding: 2.2rem 3rem;
}

.footer-middle {
  padding-top: 2rem;
  padding-bottom: 1.5rem;
  border-bottom: 1px solid rgb(39, 62, 107);
}

.footer-middle,
.footer-bottom {
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  justify-content: space-evenly;
}

.footer-menu h3 {
  display: block;
  font-size: 1.5rem;
  font-weight: bold;
  color: rgb(39, 62, 107);
  margin: 0 0 0.5rem 0;
}

.footer-menu ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.footer-menu ul li {
  margin-bottom: .4rem;
}

.footer-menu a {
  color: #47649d;
  text-decoration: none;
}

.footer-menu a:hover {
  color: #033599;
  text-decoration: underline;
}

.footer-menu a:active {
  color: rgba(71, 100, 157, 0.555);
}

.footer-bottom {
  font-family: "Montserrat", sans-serif;
  padding-top: .6rem;
  padding-bottom: 2rem;
}

/* .footer-social {

} */

.footer-social b {
  margin-right: 1rem;
  font-size: 1.5rem;
  color: rgb(39, 62, 107);
  vertical-align: middle;
}

.sr-only {
  border: 0 !important;
  clip: rect(1px, 1px, 1px, 1px) !important;
  -webkit-clip-path: inset(50%) !important;
  clip-path: inset(50%) !important;
  height: 1px !important;
  overflow: hidden !important;
  padding: 0 !important;
  position: absolute !important;
  width: 1px !important;
  white-space: nowrap !important;
}

.social-btn {
  border: 1px solid rgba(255, 255, 255, 0.1);
  display: inline-block;
  vertical-align: middle;
  width: 60px;
  height: 60px;
  color: #ffffff;
  background-image: url("./../assets/imgs/sprite.png");
  
  background-repeat: no-repeat;
}

.social-btn-vk {
  background-position: 16px -238px;
}

.social-btn-fb {
  background-position: 19px -297px;
}

.social-btn-in {
  background-position: 13px -358px;
}

.footer-copyright {
  color: #47649d;
  text-transform: uppercase;
  margin-top: 1rem;
}

.footer-copyright .heart {
  display: inline-block;
  background-image: url("./../assets/imgs/heart_icon.png");
  background-repeat: no-repeat;
  background-position: top;
  background-size: contain;
  width: 27px;
  height: 27px;
  vertical-align: middle;
}

.footer-copyright a {
  color: #47649d;
  text-decoration: none;
}

.footer-copyright a:hover {
  text-decoration: underline;
}

.footer-copyright a:active {
  color: rgba(71, 100, 157, 0.555);
}

@media (max-width: 992px) {
  .footer-social b {
    margin-right: 0;
  }
}

@media (max-width: 767px) {
  .footer-social b {
    display: none;
  }
  .footer-bottom {
    padding-bottom: 0;
  }
  .footer-middle {
    padding-top: 0;
  }
}

@media (max-width: 576px) {
  .footer-middle .footer-menu ul {
    display: none;
  }
  .footer-bottom {
    flex-direction: column;
  }
  .footer-copyright {
    margin-top: 0rem;
  }
}

@media (max-width: 480px) {
  .footer-middle {
    flex-direction: column;
    padding-bottom: 1rem;
  }
}

</style>
