<template>
  <a-scene
    mindar-image="imageTargetSrc: /card.mind; uiScanning: #scanning-overlay; uiLoading:no;"
    color-space="sRGB"
    renderer="colorManagement: true, physicallyCorrectLights"
    vr-mode-ui="enabled: false"
    device-orientation-permission-ui="enabled: false"
  >
    <a-assets>
      <img id="netpower" src="netpower.png" />
    </a-assets>

    <a-entity id="camera" position="0 0 0" rotation="0 0 0">
      <a-camera
        look-controls="enabled: true"
        cursor="fuse: false; rayOrigin: mouse;"
        raycaster="near: 0; far: 10000"
      />
    </a-entity>

    <a-plane
      onclick="alert('I was clicked')"
      color="blue"
      opaciy="0.5"
      position="0 0 0"
      height="0.552"
      width="1"
      rotation="0 0 0"
      mindar-image-target="targetIndex: 0"
    />
  </a-scene>
</template>

<script>
export default {
  name: "App",
  components: {},
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;
}
</style>
