<template>
  <div class="component">
    <h3>You may view the User Details here</h3>
    <p>Many Details</p>
    <p>User Name: {{switchName()}}</p>
    <p>User Age: {{myage}}</p>
    <button @click="resetName">Reset Name</button>
    <button @click="resetFn()">Reset Name</button>
  </div>
</template>

<script>
import { eventBus } from "../main";

export default {
  props: {
    myname: {
      type: String,
      default: "Sarah"
    },
    resetFn: {
      type: Function
    },
    myage: { Number }
  },
  methods: {
    switchName() {
      return this.myname
        .split("")
        .reverse()
        .join("");
    },
    resetName() {
      this.myname = "Bruno";
      this.$emit("nameWasReset", this.myname);
    }
  },
  created() {
    eventBus.$on("ageWasEdited", age => {
      this.myage = age;
    });
  }
};
</script>

<style scoped>
div {
  background-color: lightcoral;
}
</style>
