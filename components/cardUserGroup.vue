<template>
  <body>
    <div class="container-fluid">
      <div class="row">
        <div class="col-12 position-relative text-center">
          <h1 class="header-class">Survey Groups</h1>
        </div>
        <div class="col-lg-3 col-md-6 mt-4">
          <nuxt-link to="/user-survey-page">
            <div class="images-wrapper">
              <img src="~/assets/icon/card-img1.jpg" alt="" class="img-fluid" />
              <div class="text-paragraf">
                <h3>Group-Name</h3>
                <p>Group-Description</p>

                <p>Owner</p>
                <p>Amount-Member</p>
              </div>
            </div>
          </nuxt-link>
        </div>
        <div class="col-lg-3 col-md-6 mt-4">
          <nuxt-link to="/user-survey-page">
            <div class="images-wrapper">
              <img src="~/assets/icon/card-img1.jpg" alt="" class="img-fluid" />
              <div class="text-paragraf">
                <h3>Group-Name</h3>
                <p>Group-Description</p>

                <p>Owner</p>
                <p>Amount-Member</p>
              </div>
            </div>
          </nuxt-link>
        </div>
        <div class="col-lg-3 col-md-6 mt-4">
          <nuxt-link to="/user-survey-page">
            <div class="images-wrapper">
              <img src="~/assets/icon/card-img1.jpg" alt="" class="img-fluid" />
              <div class="text-paragraf">
                <h3>Group-Name</h3>
                <p>Group-Description</p>

                <p>Owner</p>
                <p>Amount-Member</p>
              </div>
            </div>
          </nuxt-link>
        </div>
        <div class="col-lg-3 col-md-6 mt-4">
          <nuxt-link to="/user-survey-page">
            <div class="images-wrapper">
              <img src="~/assets/icon/card-img1.jpg" alt="" class="img-fluid" />
              <div class="text-paragraf">
                <h3>Group-Name</h3>
                <p>Group-Description</p>

                <p>Owner</p>
                <p>Amount-Member</p>
              </div>
            </div>
          </nuxt-link>
        </div>
      </div>
    </div>
  </body>
</template>

<script>
export default {}
</script>

<style scoped>
.header-class {
  position: relative;
  top: 20px;
}
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