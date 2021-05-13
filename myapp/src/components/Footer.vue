<template>
  <div class="footer">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      msg: "Footer",
    };
  },
};
</script>

<style scoped>
h1 {
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100%;
  margin-bottom: 0%;
  background-image: linear-gradient(to right, rgba(141, 49, 49, 0.973), purple);
  color: black;
  text-align: center;
}
</style>
