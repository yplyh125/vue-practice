<template>
  <div>
    <h2>Hello LifeCycle</h2>
    <input type="text" v-model="username" ref="inputRef" />

    <ChildComponent
      firstname="Code"
      lastname="Scalper"
      @sendParent="sendParent"
    />
  </div>
</template>

<script>
import childComponent from "./ChildComponent.vue";
// import { ref, onMounted } from "vue";
export default {
  name: "TestComponent",
  components: { childComponent },
  methods: {
    sendParent() {
      console.log("parent event!!!");
    },
  },

  //   setup() {
  //     const inputRef = ref(null);
  //     const username = ref("scalper");
  //     onMounted(() => {
  //       inputRef.value.focus();
  //       console.log("onMounted");
  //     });
  //     return {
  //       username,
  //       inputRef,
  //     };
  //   },
};
</script>

<style></style>
