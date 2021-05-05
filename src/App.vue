<template>
  <div id="app">
    <VuePDFViewer :path="`${path}`" :fileName="`${name}`" />
  </div>
</template>
<script>
import VuePDFViewer from "@/components/VuePDFViewer";

export default {
  name: "app",
  components: {
    VuePDFViewer,
  },
  data() {
    return {
      name: "https://pdftron.s3.amazonaws.com/downloads/pl/demo.pdf", //change which pdf file loads
      path: "lib/pdfjs-2.7.570-dist/web/viewer.html", //path of the PDF.js viewer.html
    };
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
