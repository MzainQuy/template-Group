<template>
  <body class="min-vw-100 min-vh-100 position-relative">
    <div class="container-fluid content">
      <navbar />
      <firstLoginImg />
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
  margin: 0;
  padding: 0;
  background-color: #c8edff;
}
</style>