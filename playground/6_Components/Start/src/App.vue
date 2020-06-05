<template>
  <div class="container">
    <app-header></app-header>
    <div class="row">
      <app-server-status></app-server-status>
      <app-server-details></app-server-details>
    </div>
    <app-footer></app-footer>
  </div>
</template>

<script>
import Header from "./Header.vue";
import Footer from "./Footer.vue";
import ServerDetails from "./ServerDetails.vue";
import ServerStatus from "./ServerStatus.vue";

export default {
  components: {
    "app-header": Header,
    "app-footer": Footer,
    "app-server-details": ServerDetails,
    "app-server-status": ServerStatus
  }
};
</script>

<style>
</style>
