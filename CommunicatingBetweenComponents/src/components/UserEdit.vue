<template>
  <div class="component">
    <h3>You may edit the User here</h3>
    <p>Edit me!</p>
    <p>User age {{myage}}</p>
    <button @click="editAge">Edit Age</button>
    <button @click="resetAgeFn()">Edit Age</button>
  </div>
</template>

<script>
import { eventBus } from "../main";

export default {
  props: {
    myage: {
      type: Number
    },
    resetAgeFn: {
      type: Function
    }
  },
  methods: {
    editAge() {
      this.myage = 30;
      eventBus.$emit("ageWasEdited", this.myage);
    }
  }
};
</script>

<style scoped>
div {
  background-color: lightgreen;
}
</style>
