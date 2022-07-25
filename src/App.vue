<template>
  <LifecycleTest />
  <FlashingMessage message="Hello friends!" :delay="500" />
  <CongratulationsBanner :numberOfClicks="numberOfClicks" />
  <CounterButton @increment="increment" :numberOfClicks="numberOfClicks" />
  <TimerComponent @tick="onTick" name="Timer1" :delay="2000" />
  <TimerComponent @tick="onTick" name="Timer2" :delay="5000" />
  <PeopleList />
</template>

<script>
import PeopleList from "./components/PeopleList";
import CounterButton from "./components/CounterButton";
import CongratulationsBanner from "./components/CongratulationsBanner";
import LifecycleTest from "./components/LifecycleTest";
import TimerComponent from "./components/TimerComponent";
import FlashingMessage from "./components/FlashingMessage";
export default {
  name: "App",
  components: {
    PeopleList,
    CounterButton,
    CongratulationsBanner,
    LifecycleTest,
    TimerComponent,
    FlashingMessage,
  },
  data() {
    return { numberOfClicks: 0 };
  },
  methods: {
    increment() {
      this.numberOfClicks += 1;
    },
    onTick(name) {
      console.log(name + "Tick!");
    },
  },
};
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h1 {
  color: lightpink;
}
</style>
