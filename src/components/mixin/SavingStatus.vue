<template>
  <div>
    <h2>총 적금 : {{ totalMoney }}</h2>
    <button @click="addMoney(500)">500</button>
    <button @click="addMoney(1000)">1000</button>
    <button @click="addMoney(15000)">15000</button>
    <button @click="addMoney(20000)">20000</button>
  </div>
</template>

<script>
import useMoney from "../../composables/useMoney";
export default {
  name: "SavingStatus",
  setup() {
    const { addMoney, totalMoney } = useMoney(5000);

    return {
      addMoney,
      totalMoney,
    };
  },
};
</script>

<style></style>
