<template>
  <h1>This is a lifecycle test</h1>
</template>
<script>
export default {
  name: "LifecycleTest",
  props: ["numberOfClicks"],
  beforeCreate() {
    console.log("In before create");
  },
  created() {
    console.log("In created");
  },
  beforeMount() {
    console.log("In before mount");
  },
  mounted() {
    console.log("In mounted");
  },
};
</script>
