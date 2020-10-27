<template>
  <b-container class="mainContainer" fluid>
    <b-row class="navbar"><b-col cols="12">navbar</b-col></b-row>
    <b-row class="container"
      ><b-col cols="12" class="content">content</b-col></b-row
    >
    <b-row class="footer"><b-col cols="12">footer</b-col></b-row>
  </b-container>
</template>

<script>
export default {
  name: "home",
  components: {},
  data() {
    return {};
  },
};
</script>

<style scoped>
.mainContainer {
  width: 100%;
  height: 100vh;
  background-color: red;
}
</style>
