<template>
  <section class="tabs">
    <b-tabs content-class="mt-3" nav-wrapper-class="tabs-block" class="contents" fill>
      <b-tab title="О товаре" active>
        <article class="about wrapper">
          Королевский питон идеальная змея для начинающего террариумиста. Питоны не агрессивны, нетребовательны к условиям содержания. Для содержания взрослых особей подойдет горизонтальный террариум, размером 100*50*60 см. Объем можно обустроить с использованием как натуральных, так и искусственных декораций.
          В террариуме необходимо установить водоем, где питон мог бы спокойно помещаться и отмокать во время линьки. В террариуме следует разместить полки или широкие коряги, по которым змея охотно ползает. В качестве укрытий используют дуплистые коряги, свернутую в трубу кору пробкового дуба, изготовленные из досок домики с боковым или верхним входом, внутри домика кладут сфагнум. Грунт в террариуме не обязателен, но можно использовать кокосовый субстрат, сфагнум, гравий или застилать дно террариума фильтровальной бумагой. Раз в день террариум следует опрыскивать теплой водой, сфагнум увлажняют регулярно. Влажность также можно поддерживать с помощью дождевой установки, подключенной через реле времени и работающей 2-3 раза в сутки по 2-3 минуты. Лучше содержать по одному или парами. Пьют воду, для чего регулярно следует менять ее в искусственном водоеме террариума. Продолжительность жизни до 20 лет.
        </article>
      </b-tab>
      <b-tab title="Характеристики">
        <div class="wrapper">
          <table class="table properties">
            <thead>
              <tr>
                <th>Характеристика</th>
                <th>Описание</th>
              </tr>
            </thead>

            <tbody>
              <tr>
                <td>Активность</td>
                <td>сумеречная</td>
              </tr>
              <tr>
                <td>Семейство</td>
                <td>Ложноногие (Boidae)</td>
              </tr>
              <tr>
                <td>Ареал обитания</td>
                <td>Африка: от Сенегала до Нигерии и Камеруна</td>
              </tr>
              <tr>
                <td>Размер взрослого животного</td>
                <td>до 1,5 метров, самки крупнее самца</td>
              </tr>
              <tr>
                <td>Размер террариума для содержания</td>
                <td>60х45х45 см</td>
              </tr>
              <tr>
                <td>Оформление террариума</td>
                <td>укрытие, коряги, купалка</td>
              </tr>
              <tr>
                <td>Продолжительность жизни</td>
                <td>18-20 лет</td>
              </tr>
              <tr>
                <td>Рацион питания</td>
                <td>кормовые грызуны</td>
              </tr>
              <tr>
                <td>Частота кормления</td>
                <td>грызуны соответствующего размера раз в 1-3 недели</td>
              </tr>
              <tr>
                <td>Аллергия на животное</td>
                <td>может быть аллергичен</td>
              </tr>
              <tr>
                <td>Необходимое оборудование</td>
                <td>термоковрик или лампа нагрева, термометр</td>
              </tr>
              <tr>
                <td>Влажность в террариуме</td>
                <td>70-80%</td>
              </tr>
              <tr>
                <td>Возможность размножения</td>
                <td>средняя</td>
              </tr>
              <tr>
                <td>Возможность ухода за животным для ребенка</td>
                <td>средняя</td>
              </tr>
              <tr>
                <td>Контактность, общение</td>
                <td>контактный</td>
              </tr>
              <tr>
                <td>Общая температура в террариуме</td>
                <td>26-27°С</td>
              </tr>
              <tr>
                <td>Температура в точке прогрева</td>
                <td>30-32°С</td>
              </tr>
            </tbody>
          </table>
        </div>
      </b-tab>
      <b-tab title="Отзывы">
        <aside class="reviews wrapper">
          <div class="reviews-list">
            <div class="review-item">
              Спасибо магазино "Под мшистым камнем" за такую чудесную змею! больше всего мне нравится с ним гулять - ведь тогда внимание мне 100% обеспечено!
              <cite
                class="review-author"
              >Аксинья, г. Москва</cite>
            </div>

            <div class="review-item">
              Иногда мне кажется, что он просто холодная рептилия, но когда я смотрю в его бездонные глаза, то вижу в них безкрайнее море любви! и даю ему лишнюю мышку.
              Спасибо магазину "Под мшистым камнем": быстрая доставка прямо домой, хорошие консультанты(помогли выбрать терр, мышек и даже шапочку для Питоши!) и чудесные цены. Следующую змею буду покупать однозначно только у вас!
              <cite
                class="review-author"
              >Виталий, г. Санкт-Петербург</cite>
            </div>
          </div>
        </aside>
      </b-tab>
    </b-tabs>
  </section>
</template>

<script>
export default {
  name: "Tabs"
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.tabs {
  margin: 1rem 0;
  color: #47649d;
}

.nav-tabs .nav-link {
  color: #fff !important;
}

.about,
.properties,
.reviews {
  text-align: justify;
  background-color: #fff;
}

/* Характеристики */
.properties {
  text-align: left;
}

.tabs table {
  width: 80%;
  margin: 0 auto;
  border-collapse: collapse;
  border-spacing: 0;
}

.tabs th {
  padding: 0.8rem;
  border-top: none;
}

.tabs tbody {
  display: table-row-group;
  vertical-align: middle;
  border-color: inherit;
}

.tabs .table tbody tr td {
  padding: 0.8rem 1.2rem;
}

/* Отзывы */
.reviews {
  display: block;
}

.review-item {
  border-left: 3px solid #47649d;
  margin: 0 2rem 2rem 0;
  padding: 0 0 0 1.5rem;
}

.review-item p {
  margin: 0 0 1.1rem 0;
}

.review-author {
  display: block;
  font-weight: bold;
  font-style: italic;
}

/* общие стили */
.tabs .wrapper {
  padding: 1rem calc(50% - 590px);
}

.tabs .flex {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  flex-direction: column;
}
</style>

<style>
/* переопределяем бутстраповские стили: */

.tabs-block {
  margin: 1rem 0;
  background-color: rgba(223, 230, 243, 0.664);
  padding: 0;
}

.contents .mt-3,
.my-3 {
  margin: 0 2rem !important;
  font-size: 1.2rem;
}

@media (min-width: 576.98px) {
  .contents .mt-3,
  .my-3 {
    font-size: 1.3rem;
  }
}

.tabs .nav-tabs .nav-link {
  color: #47649d;
  border-color: transparent transparent rgb(71, 100, 157);
  border-width: 1px;
  font-family: "Montserrat", sans-serif;
  font-size: 1.25rem;
}

.tabs .nav-tabs .nav-link.active,
.nav-tabs .nav-item.show .nav-link {
  opacity: 1;
  color: rgb(39, 62, 107);
  font-weight: bold;
  border-color: #47649d #47649d transparent;
  font-family: "Montserrat", sans-serif;
}

.tabs .nav-tabs .nav-link:hover,
.nav-tabs .nav-link:focus {
  border-color: transparent transparent #47649d;
}

.tabs .nav-tabs .nav-link.active:hover,
.nav-tabs .nav-item.show .nav-link:focus {
  border-color: #47649d #47649d transparent;
}

.tabs .nav-tabs {
  border-bottom: 1px solid #47649d;
  padding: 0 calc(50% - 590px);
}
</style>
