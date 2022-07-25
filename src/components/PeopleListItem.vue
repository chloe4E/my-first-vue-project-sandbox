<template>
  <div>
    <h3>{{ person.name }}</h3>
    <p>Age {{ person.age }} years</p>
    <p>Hair color: {{ person.hairColor }}</p>
  </div>
</template>
<script>
export default {
  name: "PeopleListItem",
  props: ["person"], //"name", "age", "hairColor",
  /* data() {
    return {
      name: "Chloe",
      age: 123,
      hairColor: "brown",
    };
  }, */
};
</script>
