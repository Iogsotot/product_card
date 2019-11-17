<template>
    <header>
      <div class="container">
        <div class="header-top">
          <div class="header-logo"><img src="./../assets/imgs/logo.png" alt="" height="100"> <h2>Под мшистым камнем</h2></div>
          <div class="header-top-phone">
            <div class="uppercase phone-text">Наш телефон</div>
            <div><a href="tel:83152316">83152316</a> доступен с 11:00 до 11:20</div>
          </div>
        </div>
        <nav>
          <div class="menu">Меню</div>
          <ul class="header-nav uppercase">
            <li><a href="#">Наши магазины</a></li>
            <li><a href="#">Оборудование</a></li>
            <li><a href="#">Корма</a></li>
            <li><a href="#">Наполнители для туалетов</a></li>
            <li><a href="#">Каталог животных</a> </li>
          </ul>
        </nav>
      </div>

    </header>
</template>

<script>
export default {
  name: 'Header',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  header {
    background-color: rgba(223, 230, 243, 0.664);
    padding-bottom: 1rem;
    font-family: "Montserrat", sans-serif;
  }

  header > .container {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: flex-end;
  }

  .header-top {
    display: flex;
    justify-content: space-between;
    width: 100%;
    margin: 1.2rem auto 0;
    min-height: 100px;
    color: rgb(13, 46, 105);
  }

  .header-logo {
    display: flex;
    align-items: center;
    text-align: center;    
    vertical-align: middle;
    width: auto;
    height: 100px;
  }

  .header-logo h2 {
    text-align: left;
    margin: 0;
  }

  .header-logo > img {
    margin-right: 1rem;
    cursor: pointer;
  }

  .header-top-phone {
    display: flex;
    align-items: center;
    padding: .7rem 0 2px;
  }

  .phone-text {
    margin-right: 1rem;
  }

  .header-top-phone div {
    display: flex;
    flex-direction: column;
    font-size: 0.9rem;
    line-height: 1.1rem;
  }

  .header-top-phone div a {
    font-size: 2.1rem;
    color: inherit;
    font-weight: bold;
    text-transform: uppercase;
    text-decoration: none;
    line-height: 2rem;
    text-align: right;
    word-wrap: nowrap;
  }

  .header-nav {
    font-size: 0.9rem;
    display: flex;
    justify-content: flex-end;
    padding: 0;
    margin: 1.5rem 0 0;

    list-style: none;
  }

  .header-nav li {
    font-weight: bolder;
    margin-left: 2.5rem;
  }

  .header-nav li:last-child {
    margin-right: 0;
  }

  .header-nav a {
    cursor: pointer;
    text-decoration: none;
    color: inherit;
  }

  .header-nav a:hover {
    text-decoration: underline;
    text-shadow: 0 0 .5px #0d2e69, 0 0 .6px #0d2e69, 0 0 .6px #0d2e69; 
  }
  
  .header-nav a:active {
    color: rgba(13, 46, 105, 0.5);
    text-decoration: underline;
  }

  .uppercase {
    text-transform: uppercase;
  }

   nav .menu {
    display: none;
    cursor: pointer;
    text-decoration: none;
    font-weight: bold;
    font-size: large;
    color: inherit;
    margin-bottom: 1rem;
  }

  nav .menu:hover {
    text-decoration: underline;
    text-shadow: 0 0 .5px #0d2e69, 0 0 .6px #0d2e69, 0 0 .6px #0d2e69; 
  }
  
  nav .menu:active {
    color: rgba(13, 46, 105, 0.5);
    text-decoration: underline;
  }

@media (max-width: 575.98px){
  .header-logo h2 {
    display: none;
  }

  .header nav ul {
    display: none;
  }

  .header nav .menu {
    display: block;
  }
}

@media (max-width: 767.98px){
    .header-nav li {
    margin-left: 1.5rem;
    }
    .header-logo {
      margin-right: 2rem;
    }

  .header-top-phone .phone-text {
   text-align: right;
   margin-right: .7rem;
  }

  .header-top-phone div {
    align-items: center;
  }
    
}


</style>
