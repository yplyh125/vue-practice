<template>
  <div>
    <h2>child Component</h2>
    <input type="text" v-model="username" />
  </div>
</template>

<script>
export default {
  name: "childComp",
  data() {
    return {
      username: "",
    };
  },
  methods: {
    sayHello() {
      console.log("say Hello");
    },
  },
  beforeCreate() {
    console.log("child beforeCreate");
  },
  created() {
    console.log("child created");
  },
  beforemounted() {
    console.log("child beforemounted");
  },
  mounted() {
    console.log("child mounted");
  },
  beforeUpdate() {
    console.log("child beforeUpdate");
  },
  updated() {
    console.log("child updated");
  },
  beforeUnmount() {
    console.log("child beforeUnmount");
  },
  unmounted() {
    console.log("child unmounted");
  },
};
</script>

<style></style>
