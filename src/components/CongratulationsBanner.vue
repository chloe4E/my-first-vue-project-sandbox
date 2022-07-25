<template>
  <h1 v-if="numberOfClicks >= 10">
    You've reach {{ numberOfClicks }} clicks : awesome
  </h1>
</template>

<script>
export default {
  name: "CongratulationsBanner",
  props: ["numberOfClicks"],
};
</script>
