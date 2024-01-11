<template>
  <div>
    <hr />
    <h3>{{ fullname }}</h3>
    <button @click="sendparent">child click</button>
  </div>
</template>

<script>
import { computed } from "vue";
export default {
  name: "childComponent",
  props: ["firstname", "lastname"],
  setup(props, context) {
    console.log(context);
    const fullname = computed(() => {
      return `${props.firstname} ${props.lastname}`;
    });
    function sendparent() {
      context.emit("sendParent");
    }
    return {
      fullname,
      sendparent,
    };
  },
};
</script>

<style></style>
