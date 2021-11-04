<template>
  <div
    class="container-fluid content-icon mt-5"
    v-if="!show"
    @click="show = true"
  >
    <div class="container">
      <div class="text-content text-left ml-5 mb-2 text-center">
        <div class="paragraf">
          <h2>Looks like you don't have the survey group</h2>
          <p>want to join a survey group or create a new one?</p>
        </div>
      </div>
      <div class="image-content d-flex justify-content-center mt-4">
        <img width="700" src="~/assets/image/site-stats.svg" alt="" />
      </div>
    </div>
  </div>
  <card-user-group v-else />
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
.paragraf {
  margin-top: 60px;
}
.paragraf p {
  font-weight: 400;
}
.paragraf h2 {
  font-weight: bold;
}

@media only screen and (max-width: 675px) {
  .image-content {
    margin-top: -520px;
  }
  img {
    margin-top: 20px;

    width: 500px;
  }
}
@media only screen and (max-width: 525px) {
  img {
    width: 350px;
  }
  .paragraf {
    margin-left: -20px;
    text-align: left;
    margin-right: 35px;
  }
  .paragraf h2 {
    line-height: 1.6;
    font-size: 35px;
  }
  .paragraf p {
    font-size: 24px;
  }
}
</style>