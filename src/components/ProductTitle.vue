<template>
  <div class="product_title">
      <h1>{{msg}} <span class="new">Новинка!</span></h1>
      <div class="vendor_code">78921389</div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    
    .product_title {
          text-align: left;
    }

    h1 {
        font-weight: bold;
    }

    .new {
        display: inline-block;
        font-weight: normal;
        font-size: 1rem;
        vertical-align: top;
        background-color: rgba(248, 180, 53, .6);
        padding: 5px 10px;
        border: 1px solid rgba(248, 180, 53, .6);
        border-radius: 7px;
        color: rgb(180, 6, 6);
    }

    .vendor_code {
        font-size: 0.8rem;
        line-height: 2rem;
        padding-top: .2rem;
        text-align: right;
    }

    .vendor_code:before{
        content: 'Артикул: ';
    }
</style>
