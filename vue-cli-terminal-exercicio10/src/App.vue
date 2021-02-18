<template>
  <div id="app">
    <ul>
      <li v-for="(item, index) in toDos" :key="index">
        {{ item }} e {{ index }}
      </li>

      <li v-for="(item, index) in toDos2" :key="index">
        {{ item }} e {{ index }}
      </li>
      <template v-if="toDos3.lenght > 0">
        <li v-for="(toDos3, index) in filteredToDos3" :key="index">
          {{ toDos3 }} e {{ index }}
        </li>
      </template>
      <li v-else> Nenhum item</li>
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
        item1: "item 1",
        item2: "item 2",
        item3: "item 3",
      },
      toDos3: [
        { label: "ToDO 1", isCompleted: false },
        { label: "ToDO 2", isCompleted: false },
        { label: "ToDO 3", isCompleted: true },
        { label: "ToDO 4", isCompleted: true },
      ],
    };
  },
  computed: {
    filteredToDos3() {
      return this.toDos3.filter((toDo3) => !toDo3.isCompleted);
    },
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
