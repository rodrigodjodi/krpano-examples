<template>
  <div id="pano" style="width: 100%; height: 600px;"></div>
</template>

<script>


export default {
  layout: 'examples',
  head: {
      script: [
      { src: 'krpano.js'  }
    ],
  },
  mounted() {
      embedpano({
          xml: "krpano.xml",
        target: "pano",
        html5: "only",
        initvars: {
          editmode: "true"
        },
        // onready: krpanoReady,
        mobilescale: 1.0,
        passQueryParameters: true
      });
  }
}
</script>

<style>

</style>
