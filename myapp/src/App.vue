<template>
  <div class="main">
    <Header />
    <h1 class="title">Body</h1>
    <Body />
    <Footer />
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Body from "./components/Body.vue";

export default {
  name: "App",
  components: {
    Header,
    Body,
    Footer,
  },
};
</script>

<style>
.title {
  text-align: center;
  padding-top: 10%;
  position: inherit;
}
</style>
