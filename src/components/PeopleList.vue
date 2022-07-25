<template>
  <h1>People List:</h1>
  <PeopleListItem :person="person1" />
  <PeopleListItem :person="person2" />
  <PeopleListItem :person="person3" />
</template>

<script>
import PeopleListItem from "./PeopleListItem";
export default {
  name: "PeopleList",
  components: {
    PeopleListItem,
  },
  data() {
    return {
      person1: { name: "Chloe", age: 123, hairColor: "brown" },
      person2: { name: "Maeddine", age: 124, hairColor: "black" },
      person3: { name: "Axelle", age: 1, hairColor: "auburn" },
    };
  },
};
</script>
