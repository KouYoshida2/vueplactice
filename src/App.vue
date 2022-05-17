<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld @parent="parent" msg="propsで書き換えました。" />
</template>

<script>
import HelloWorld from "@/components/HelloWorld";

export default {
  name: "App",
  components: {
    HelloWorld,
  },
  methods: {
    parent: function (e) {
      console.log(e);
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
