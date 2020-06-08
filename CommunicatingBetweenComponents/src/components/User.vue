<template>
  <div class="component">
    <h1>The User Component</h1>
    <p>I'm an awesome User!</p>
    {{name}}
    <button @click="changeName">Change Name</button>
    <hr />
    <div class="row">
      <div class="col-xs-12 col-sm-6">
        <app-user-detail
          :myage="age"
          :myname="name"
          :resetFn="resetName"
          @nameWasReset="name = $event"
        ></app-user-detail>
      </div>
      <div class="col-xs-12 col-sm-6">
        <app-user-edit :myage="age" :resetAgeFn="editAge"></app-user-edit>
      </div>
    </div>
  </div>
</template>

<script>
import UserDetail from "./UserDetail.vue";
import UserEdit from "./UserEdit.vue";

export default {
  data() {
    return {
      name: "Bruno",
      age: 20
    };
  },
  methods: {
    changeName() {
      this.name = "Sarah";
    },
    resetName() {
      this.name = "Bruno";
    },
    editAge() {
      this.age = 30;
    }
  },
  components: {
    appUserDetail: UserDetail,
    appUserEdit: UserEdit
  }
};
</script>

<style scoped>
div {
  background-color: lightblue;
}
</style>
