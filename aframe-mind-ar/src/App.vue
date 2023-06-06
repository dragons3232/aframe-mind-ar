<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Welcome to Your Vue.js App" />
  <a-scene>
    <a-assets>
      <img id="netpower" src="netpower.png" />
    </a-assets>

    <a-entity id="camera" position="0 0 0" rotation="-20 0 0">
      <a-camera
        look-controls="enabled: true"
        cursor="fuse: false; rayOrigin: mouse;"
        raycaster="near: 0; far: 10"
      />
    </a-entity>

    <a-box position="0 -1 -2" rotation="0 30 0" material="src: netpower.png" />
    <a-sky color="#ECECEC"></a-sky>
  </a-scene>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
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
