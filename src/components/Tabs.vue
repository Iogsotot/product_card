<template>
  <section class="tabs ">
    <div class="container">
      <b-tabs content-class="mt-3" fill>
        <b-tab title="О товаре" active>
          <p>I'm the first tab</p>
        </b-tab>
        <b-tab title="Характеристики">
          <p>I'm the second tab</p>
        </b-tab>
        <b-tab title="Отзывы">
          <p>I'm the tab with the very, very long title</p>
        </b-tab>
      </b-tabs>
    </div>
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
    color: #47649D;
  }

  .nav-tabs .nav-link {
    color: #fff !important;
  }

  .container {
  padding: 0 calc(50% - 590px);
}
</style>

<style>
  .tabs .nav-tabs .nav-link {
    color: #47649D;
    border-color: transparent  transparent #47649D;
    border-width: 2px;
  }

  .tabs .nav-tabs .nav-link.active, .nav-tabs .nav-item.show .nav-link {
    opacity: .7;
    color: rgb(39, 62, 107);
    font-weight: bold;
    border-color: #47649D #47649D transparent;
  }

  .tabs .nav-tabs .nav-link:hover, .nav-tabs .nav-link:focus {
    border-color: transparent  transparent #47649D;
  }

  .tabs .nav-tabs .nav-link.active:hover, .nav-tabs .nav-item.show .nav-link:focus {
    border-color: #47649D #47649D transparent;
  }
</style>
