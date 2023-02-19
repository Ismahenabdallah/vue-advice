<template>
  <page-header :title="title" :text="text"> </page-header>
  <page-form></page-form>
</template>

<script>
import PageHeader from "./components/PageHeader.vue";
import PageForm from "./components/PageForm.vue";
import quotes from "../data.json";
export default {
  name: "App",
  components: {
    PageHeader,
    PageForm,
  },
  provide() {
    return {
      dataJson: this.quotes,
    };
  },
  data() {
    return {
      quotes,
    };
  },
};
</script>

<style>
@import "./assets/css/style.css";
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
