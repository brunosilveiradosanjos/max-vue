<template>
  <div id="app">
    <app-quote>
      <h2>The Quote</h2>
      <p>A wonderful Quote</p>
    </app-quote>
    <img alt="Vue logo" src="./assets/logo.png" />
  </div>
</template>

<script>
import Quote from "./components/Quote.vue";

export default {
  name: "App",
  components: {
    appQuote: Quote
  }
};
</script>

<style scoped>
div {
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
