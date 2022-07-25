<template>
  <h1>People List:</h1>
  <!--   <PeopleListItem :person="person1" />
  <PeopleListItem :person="person2" />
  <PeopleListItem :person="person3" /> -->
  <PeopleListItem
    v-for="person in people"
    :key="person.name"
    :person="person"
  />
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
      people: [
        { name: "Chloe", age: 123, hairColor: "brown" },
        { name: "Maeddine", age: 124, hairColor: "black" },
        { name: "Axelle", age: 1, hairColor: "auburn" },
      ],
    };
    /* {
      person1: { name: "Chloe", age: 123, hairColor: "brown" },
      person2: { name: "Maeddine", age: 124, hairColor: "black" },
      person3: { name: "Axelle", age: 1, hairColor: "auburn" },
    }; */
  },
};
</script>

<style scoped>
h1 {
  color: lightseagreen;
}
</style>
