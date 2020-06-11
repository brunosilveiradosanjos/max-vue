<template>
  <div>
    <h3>New Quote</h3>
    <button @click="counter++">Counter</button>
    <p>{{counter}}</p>
  </div>
</template>
<script>
export default {
  data() {
    return {
      counter: 0
    };
  },
  //   By default the component will be destroyed when other were selected
  destroyed() {
    console.log("New was destroyed");
  }
};
</script>