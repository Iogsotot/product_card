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
  padding: 3.2rem 0 3.6rem;
}

.footer-top {
  margin-bottom: 3.2rem;
}

.footer-logo {
  /* width: 205px;
  height: 55px; */
}

.footer-logo img {
  /* width: 205px;
  height: 55px; */
}

.footer-middle {
  padding-top: 3.6rem;
  margin-bottom: 3.6rem;
}

.footer-middle,
.footer-bottom {
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  justify-content: space-evenly;
  border-top: 1px solid #5e5e5e;
}

.footer-menu {
  margin-right: 1.4rem;
}

.footer-menu h3 {
  font-family: "Georgia", serif;
  display: block;
  font-size: 1.7rem;
  font-weight: bold;
  color: rgb(39, 62, 107);
  margin: 0 0 1.4rem 0;
}

.footer-menu ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.footer-menu ul li {
  margin-bottom: 1rem;
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
  color: rgba(255, 255, 255, 0.3);
}

.footer-bottom {
  padding-top: 3.6rem;
}

/* .footer-social {

} */

.footer-social b {
  margin-right: 2.5rem;
  font-size: 1.7rem;
  font-family: "Georgia", serif;
  color: rgb(39, 62, 107);
  font-weight: bold;
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
  /* margin-right: 0.8rem; */
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
  margin-top: 17px;
}

.footer-copyright .heart {
  display: inline-block;
  background-image: url("./../assets/imgs/heart_icon.png");
  background-repeat: no-repeat;
  background-position: center;
  background-size: contain;
  width: 27px;
  height: 24px;
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
  color: rgba(255, 255, 255, 0.3);
}

</style>
