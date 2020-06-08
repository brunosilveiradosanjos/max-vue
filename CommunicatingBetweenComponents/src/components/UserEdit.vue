<template>
  <div class="component">
    <h3>You may edit the User here</h3>
    <p>Edit me!</p>
    <p>User age {{myage}}</p>
    <button @click="resetAgeFn()">Edit Age</button>
  </div>
</template>

<script>
export default {
  props: {
    myage: {
      type: Number
    },
    resetAgeFn: {
      type: Function
    }
  }
};
</script>

<style scoped>
div {
  background-color: lightgreen;
}
</style>
