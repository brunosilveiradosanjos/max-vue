<template>
  <div class="ma-2 pa-2">
    <v-btn x-large class="grey lighten-2">
      <div class="panel-body">
        <slot></slot>
      </div>
    </v-btn>
  </div>
</template>

<script>
export default {
  props: ["quotes"]
};
</script>


<style scoped>
.panel-body {
  font-family: "Arizonia", cursive;
  text-transform: lowercase;
  font-size: 30px;
}
/* .quote {
  cursor: pointer;
}
.quote:hover {
  background-color: #ffe2e2;
} */
</style>
