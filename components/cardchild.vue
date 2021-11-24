<template>
  <div class="images-wrapper">
    <img src="~/assets/icon/card-img1.jpg" alt="" class="img-fluid" />
    <div class="text-paragraf">
      <h3>{{ groupChild.group_name }}</h3>
      <p>{{ groupChild.group_desc }}</p>

      <p>Owner</p>
      <p>Amount-Member</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    groupChild: Object,
  },
}
</script>

<style scoped>
.images-wrapper {
  position: relative;
}
.images-wrapper img {
  border-radius: 20px;
  transition: 5s;
}
.images-wrapper img:hover,
.text-paragraf:hover {
  cursor: pointer;
  width: 95%;
  height: 95%;
}
.text-paragraf {
  line-height: 1;
  padding: 13px;
  margin-left: 5px;
  color: azure;
  position: absolute;
  top: 0;
}
</style>