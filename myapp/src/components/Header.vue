<template>
  <div class="header">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      msg: "Header",
    };
  },
};
</script>

<style scoped>
h1 {
  background-image: linear-gradient(to right, rgba(141, 49, 49, 0.973), purple);
  text-align: center;
  width: 100%;
  top: 0;
  left: 0;
  margin-top: 0%;
  position: fixed;
}
</style>
