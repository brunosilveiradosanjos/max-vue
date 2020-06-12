<template>
  <div class="container">
    <div class="col-xs-12">
      <br />
      <button @click="selectedComponent='appGreen'" class="btn btn-success">Load Green Template</button>
      <button @click="selectedComponent='appBlue'" class="btn btn-primary">Load Blue Template</button>
      <button @click="selectedComponent='appRed'" class="btn btn-danger">Load Red Template</button>
      <hr />
      <component :is="selectedComponent">
        <p>The Selected Component is {{selectedComponent}}</p>
      </component>
      <img alt="Vue logo" src="./assets/logo.png" />
    </div>
  </div>
</template>

<script>
import "bootstrap/dist/css/bootstrap.css";

import Blue from "./components/Blue.vue";
import Green from "./components/Green.vue";
import Red from "./components/Red.vue";

export default {
  data() {
    return {
      selectedComponent: "appRed"
    };
  },
  components: {
    appBlue: Blue,
    appGreen: Green,
    appRed: Red
  }
};
</script>

<style scoped>
.container {
  text-align: center;
}
div {
  text-align: center;
}
</style>
