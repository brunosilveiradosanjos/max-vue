<template>
  <li
    @click="serverSelected"
    style="cursor: pointer"
    class="list-group-item"
  >Server # {{ server.id }}</li>
</template>
<script>
import { serverBus } from "../main";

export default {
  props: {
    server: { type: Object, default: "Unknown" }
  },
  methods: {
    serverSelected() {
      serverBus.$emit("serverSelected", this.server);
    }
  }
};
</script>