<template>
  <div id="app">
    <ul>
      <li v-for="(item, index ) in toDos" :key="index">
        {{ item }} e {{index}}
        <li v-for="(item, index ) in toDos2" :key="index">
        {{ item }} e {{index}}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {
      toDos: ["item 1", "item 2", "item 3"],
      toDos2: {
        item1: 'item 1',
        item2: 'item 2',
        item3: 'item 3',
      },
    };
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
