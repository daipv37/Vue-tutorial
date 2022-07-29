<template>
  <div id="app">
    <div class="container">
      <button v-on:click="title = 'LSoM best RIVEN'">
        Change #app
      </button>
      <comp-header
        v-bind:title="title"
        v-on:changeTitleEvent="handleChangeTile"
      />
      <list-user
        v-on:handleDeleteUser="handleDeleteUser" 
        v-bind:listUsers="listUsers" />
      <comp-footer 
        v-bind:title="title"
      />
    </div>
  </div>
</template>

<script>
import CompHeader from "./components/CompHeader.vue";
import CompFooter from "./components/CompFooter.vue";
import ListUser from "./components/ListUser.vue";
/*
App
  Header
  ListProduct
    Product
    Product
    Product
    Product
    Product
    Product
  Footer
*/
export default {
  components: { CompHeader, CompFooter, ListUser },
  name: "app",
  data() {
    return {
      title: "Anh Dai dep trai",
      listUsers: [
        { id: 1, email: "test@gmail.com", isActice: true },
        { id: 2, email: "test@gmail.com", isActice: true },
        { id: 3, email: "test@gmail.com", isActice: true },
        { id: 4, email: "test@gmail.com", isActice: true },
        { id: 5, email: "test@gmail.com", isActice: true },
        { id: 6, email: "test@gmail.com", isActice: true },
        { id: 7, email: "test@gmail.com", isActice: true },
        { id: 8, email: "test@gmail.com", isActice: true },
        { id: 9, email: "test@gmail.com", isActice: true },
        { id: 10, email: "test@gmail.com", isActice: true },
        { id: 11, email: "test@gmail.com", isActice: true },
        { id: 12, email: "test@gmail.com", isActice: true },
        { id: 13, email: "test@gmail.com", isActice: true },
        { id: 14, email: "test@gmail.com", isActice: true },
        { id: 15, email: "test@gmail.com", isActice: true },
        { id: 16, email: "test@gmail.com", isActice: true },
      ],
    };
  },
  methods: {
    handleChangeTile() {
      this.title = "Lorem ipsum dolor sit amet consectetur adipisicing elit. Laborum ullam placeat eaque optio facilis, architecto esse molestiae excepturi! Cupiditate maxime tempora, repellat debitis porro fugit voluptatem quod eos est repudiandae.";
    },
    handleDeleteUser(data) {
      console.log(data);
    }
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
