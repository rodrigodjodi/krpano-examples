<template>
  <div id="pano" style="width: 100%; height: 100%;"></div>
</template>

<script>

import xml from "~/assets/folder-xml.js"
export default {
  layout: 'examples',
  head: {
      script: [
      { src: 'krpano.js'  }
    ],
  },
  computed:{
    xml() {
      return `examples/${this.$route.params.example}/${xml[this.$route.params.example]}`
    }
  },
  mounted() {
      embedpano({
        xml: this.xml,
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
