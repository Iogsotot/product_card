<template>
  <div class="product_title">
    <h1>
      {{title}}
      <span class="new">New!</span>
    </h1>
    <div class="vendor_code">78921389</div>
  </div>
</template>

<script>
export default {
  name: "product_title",
  data() {
    return {
      title: "Королевский питон"
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.product_title {
  text-align: center;
}

h1 {
  font-weight: bold;
  margin: 0.8rem 0 0;
}

.new {
  display: inline-block;
  padding: 5px 10px;

  border-radius: 15px;

  font-size: 1rem;
  vertical-align: top;
  color: #ffffff;

  background-color: rgba(240, 173, 78); 
}

.vendor_code {
  padding-top: 0.2rem;

  font-size: 1rem;
  line-height: 2rem;
  font-weight: 100;
  text-align: right;
  color: #727272;
}

.vendor_code:before {
  content: "Артикул: ";
}
</style>
