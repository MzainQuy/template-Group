<template>
  <body class="min-vw-100 min-vh-100 position-relative">
    <div class="container-fluid content">
      <navbar />

      <card-user-group />
    </div>
  </body>
</template>

<script>
import cardUserGroup from '~/components/cardUserGroup.vue'

export default {
  components: { cardUserGroup },
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