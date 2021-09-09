<template>
  <div id="app">
    <h2>Количество страниц: {{ pageCount }}</h2>
    <div class="pdf-content">
      <pdf src="./lorem-ipsum.pdf" @num-pages="pageCount = $event"></pdf>
    </div>
  </div>
</template>

<script>
import pdf from 'vue-pdf';

export default {
  name: 'App',
  components: {
    pdf
  },
  data() {
    return {
      pageCount: 0
    }
  },
  methods: {}
}
</script>

<style>
@import "./assets/css/style.min.css";
.pdf-content {
  width: 600px;
  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
</style>
