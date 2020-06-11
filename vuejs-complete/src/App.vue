<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12">
        <button @click="selectedComponent = 'appQuote'">Quote</button>
        <button @click="selectedComponent = 'appAuthor'">Author</button>
        <button @click="selectedComponent = 'appNew'">New</button>
        <p>{{selectedComponent}}</p>
        <hr />
        <div v-if="selectedComponent != 'appQuote'">
          <component :is="selectedComponent"></component>
        </div>
        <div v-if="selectedComponent=='appQuote'">
          <app-quote>
            <h2 slot="title">{{quoteTitle}}</h2>
            <p>A wonderful Quote</p>
          </app-quote>
        </div>
      </div>
    </div>
    <img alt="Vue logo" src="./assets/logo.png" />
  </div>
</template>

<script>
import Quote from "./components/Quote.vue";
import Author from "./components/Author.vue";
import New from "./components/New.vue";

export default {
  data() {
    return {
      quoteTitle: "The Quote",
      selectedComponent: "appQuote"
    };
  },
  components: {
    appQuote: Quote,
    appAuthor: Author,
    appNew: New
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
