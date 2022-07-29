<template>
  <header>
    <h1>{{ title }}</h1>
    <button v-on:click="changeTitleFooter">Click me</button>
  </header>
</template>

<script>
export default {
  name: "comp-header",
  props: {
    title: {
      type: String,
    },
  },
  data() {
    return {
      
    };
  },
  methods: {
    changeTitleFooter(e) {
      this.$emit("changeTitleEvent");
    },
  },
};
</script>

<style>
</style>