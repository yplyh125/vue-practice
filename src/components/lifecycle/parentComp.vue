<template>
  <div>
    <h2>parent Component</h2>
    <input v-model="nickname" ref="inputRef" />
    <button @click="consoleRef">consoleeeee ref</button>
    <hr />
    <ChildComp v-if="showChild" />
    <button @click="showChild = false">unmount child</button>
  </div>
</template>

<script>
import ChildComp from "./ChildComp.vue";
export default {
  name: "parentComp",
  data() {
    return {
      nickname: "",
      showChild: true,
    };
  },
  methods: {
    consoleRef() {
      console.log(this.$refs.inputRef, "input ref");
      console.log(this.$refs.ChildComp, "Child Comp");
      this.$refs.ChildComp.sayHello();
    },
  },
  components: { ChildComp },
  beforeCreate() {
    console.log("parent beforeCreate");
  },
  created() {
    console.log("parent created");
  },
  beforemounted() {
    console.log("parent beforemounted");
  },
  mounted() {
    console.log("parent mounted");
  },
  beforeUpdate() {
    console.log("parent beforeUpdate");
  },
  updated() {
    console.log("parent updated");
  },
  beforeUnmount() {
    console.log("parent beforeUnmount");
  },
  unmounted() {
    console.log("parent unmounted");
  },
};
</script>

<style></style>
