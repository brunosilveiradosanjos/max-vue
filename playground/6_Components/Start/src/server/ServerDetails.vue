<template>
  <div class="col-xs-12 col-sm-6">
    <p v-if="!server">Please select a server</p>
    <p v-else>Server: {{server.id}} - Status: {{server.status}}</p>
    <hr />
    <button @click="setNormal">Set Normal</button>
  </div>
</template>
<script>
import { serverBus } from "../main";

export default {
  data() {
    return {
      server: null
    };
  },
  created() {
    serverBus.$on("serverSelected", server => {
      this.server = server;
    });
  },
  methods: {
    setNormal() {
      this.server.status = "Normal";
    }
  }
};
</script>