<template>
  <body>
    <div class="container-fluid">
      <navbar />
      <firstLoginImg />
      <div class="container-fluid fixed-bottom">
        <footer class="footer">
          <img src="~assets/image/wave-up.svg" alt="" class="wave-image" />
        </footer>
      </div>
    </div>
  </body>
</template>

<script>
export default {
  data() {
    return {
      show: false,
    }
  },
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,900;1,300;1,500&display=swap');

body {
  margin-top: -10px;
  width: 100%;
  height: 1200px;
  background-color: #c8edff;
}

.footer {
  position: relative;
  top: 162px;
  left: -120px;
  min-width: 2000px;
}
</style>