<template>
  <div id="app">
    <b-container fluid class="bv-example-row mb-4" >
      <img alt="logo" width="15%" src="./assets/2.png" />
    </b-container>
    <br />
    <music />
  </div>
</template>
<script>
import music from "./components/music";
export default {
  name: "App",
  components: {
  music,
  }
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
body {
  background-image: url("./assets/4.jpg");
  background-attachment: fixed;
  background-repeat: no-repeat;
  background-size: 100% 100%;
  height: 100vh;
}
.key{
    width: 500px;
    height: 50px;
    font: 1.5em sans-serif;
    color: rgb(29, 164, 226);
    border: 2px solid #09462e;
    box-shadow: none;
    border-block: 24px;
}
/* body {background: bottom;} */

</style>
