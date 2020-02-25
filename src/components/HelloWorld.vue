<template>
  <div class="hello">
    <ul>
      <!-- Elements in iteration expect to have 'v-bind:key' directives. -->
      <!-- avoid using non-primitive value as key: v-bind:key="entry" -->
      <li v-for="entry in entries" class="list-item" v-bind:key="entry.content">{{ entry.content }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      entries: [{ content: "a" }, { content: "b" }, { content: "c" }]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.list-item {
  background: white;
  color: gray;
  padding: 20px;
  margin: 20px;
}
ul {
  background: tomato;
  width: 400px;
  height: 400px;
}
</style>
