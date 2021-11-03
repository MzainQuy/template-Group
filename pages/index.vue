<template>
  <div class="container-fluid">
    <div class="ml-5 mt-2 header-title">
      <h1 class="header-title">Survey.In</h1>
    </div>

    <div class="container-fluid mt-5 p-5">
      <div class="row">
        <div class="col-lg-6 align-self-center col-md-12">
          <div class="h2-wrapp">
            <h2>Buat survey <span>bersama</span> dalam <span>Grup</span>.</h2>
          </div>
          <div class="paragrag-wrap">
            <p class="paragraf">
              Survey.in is an application for making surveys in a Group! Buat
              grup, Undang pengguna, dan buat Survey secara
            </p>
          </div>
          <div class="button-wrap">
            <nuxt-link to="/registrasion">
              <button type="" class="button">Register</button>
            </nuxt-link>
            <nuxt-link to="/login">
              <button type="" class="button">Login</button>
            </nuxt-link>
          </div>
        </div>
        <div class="col-lg-5 image-wrapp mt-4 text-center">
          <img
            src="~assets/image/Data-Reports.svg"
            alt=""
            class="image"
            width="600"
          />
        </div>
      </div>
    </div>
    <footer class="footer">
      <img src="~assets/image/wave-up.svg" alt="" class="wave-image" />
    </footer>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,900;1,300;1,500&display=swap");
span {
  color: #009ee2;
}

.header-title {
  font-family: "Roboto", sans-serif;
  color: #009ee2;
  font-size: 37px;
}

.h2-wrapp h2 {
  font-family: "Roboto", sans-serif;
  font-size: 60px;
  font-weight: bold;
}

.button {
  width: 140px;
  height: 37px;
  background-color: #009ee2;
  color: aliceblue;
  border-radius: 10px;
  border: 1px solid;
}

.footer {
  position: fixed;
  right: 0.5px;
  min-width: 1440px;
}
.footer img {
  min-width: 1440px;
}

@media only screen and (max-width: 780px) {
  .button {
    width: 120px;
    height: 37px;
    font-size: 20px;
  }
  .image-wrapp {
    margin-top: 10px;
    padding: 25px;
  }
  .footer {
    display: none;
  }
}

@media only screen and (max-width: 660px) {
  .header-title {
    font-size: 52px;
    font-weight: 500;
  }
  .button-wrap {
    width: 360px;
  }
  .button {
    width: 150px;
    height: 42px;
    font-size: 20px;
  }
  .h2-wrapp {
    width: 500px;
  }
  .h2-wrapp h2 {
    line-height: 1.2;
    font-size: 68px;
  }
  .paragrag-wrap {
    width: 500px;
  }
  .paragraf {
    font-size: 32px;
  }
  .footer {
    display: none;
  }
}

@media only screen and (max-width: 480px) {
  .header-title {
    font-size: 52px;
    font-weight: 500;
  }
  .button-wrap {
    width: 500px;
  }
  .button {
    width: 200px;
    height: 50px;
    font-size: 20px;
  }
  .h2-wrapp {
    margin-top: -30px;
    width: 380px;
  }
  .h2-wrapp h2 {
    line-height: 1.4;
    font-size: 68px;
  }
  .paragrag-wrap {
    width: 350px;
  }
  .paragraf {
    line-height: 1.7;
    font-size: 34px;
    font-weight: bold;
  }
  .footer {
    display: none;
  }
  .image {
    display: none;
  }
}
</style>