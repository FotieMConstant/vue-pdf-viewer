<template>
  <div class="pdf-container">
    <iframe height="100%" width="100%" :src="`${getFilePath}`"></iframe>
  </div>
</template>

<script>
export default {
  name: "PDFViewer",
  props: {
    fileName: String,
    path: String,
  },
  computed: {
    getFilePath() {
      if (this.fileName !== "") {
        return this.path + "?file=" + this.fileName;
      }
      return this.path;
    },
  },
};
</script>
<style scoped>
.pdf-container iframe {
  border: 0px solid black;
  width: 100%;
  height: 79vh;
  min-width: 400px;
}
</style>