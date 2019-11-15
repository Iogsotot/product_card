<template>
  <section>
    <div>
      <b-tabs content-class="mt-3" fill>
        <b-tab title="First" active>
          <p>I'm the first tab</p>
        </b-tab>
        <b-tab title="Second">
          <p>I'm the second tab</p>
        </b-tab>
        <b-tab title="Very, very long title">
          <p>I'm the tab with the very, very long title</p>
        </b-tab>
        <b-tab title="Disabled" disabled>
          <p>I'm a disabled tab!</p>
        </b-tab>
      </b-tabs>
    </div>
  </section>
</template>

<script>
export default {
  name: "Tabs",
  props: {
    msg: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
