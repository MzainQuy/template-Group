<template>
  <div class="container-fluid">
    <div class="ml-2 mt-1 wrapp-titleH">
      <h1 class="header-title">Survey.In</h1>
    </div>

    <div class="container-fluid p-4">
      <div class="row mt-5">
        <div class="col-lg-6 align-self-center col-md-12 pt-4 ml-1">
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
              <button type="" class="button mr-2">Register</button>
            </nuxt-link>
            <nuxt-link to="/login">
              <button type="" class="button">Login</button>
            </nuxt-link>
          </div>
        </div>
        <div class="col-lg-5 image-wrapp text-center mr-4">
          <img
            src="~assets/image/Data-Reports.svg"
            alt=""
            class="image"
            width="650"
          />
        </div>
      </div>
    </div>
    <footer class="footer mt-2">
      <img src="~assets/image/wave-up.svg" alt="" class="wave-image" />
    </footer>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,900;1,300;1,500&display=swap');
span {
  color: #009ee2;
}

.header-title {
  font-family: 'Roboto', sans-serif;
  color: #009ee2;
  font-size: 3.3rem;
  font-weight: 510;
}

.h2-wrapp h2 {
  font-family: 'Roboto', sans-serif;
  font-size: 4.3rem;
  font-weight: bold;
}
.paragraf {
  font-size: 1.5rem;
  font-weight: 300;
}
.button {
  width: 170px;
  height: 40px;
  background-color: #009ee2;
  color: aliceblue;
  border-radius: 10px;
  border: 1px solid;
  font-weight: 500;
  font-size: 1.2rem;
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
  .image-wrapp {
    margin-top: 10px;
    padding: 25px;
  }
  .footer {
    display: none;
  }
}

/*  */

@media only screen and (max-width: 580px) {
  .h2-wrapp {
    width: 450px;
  }
  .h2-wrapp h2 {
    margin-top: -64px;
    font-size: 4.8rem;
    letter-spacing: 2px;
  }
  .paragrag-wrap {
    width: 350px;
  }
  .paragraf {
    font-weight: 600;
    letter-spacing: 4px;
    font-weight: bold;
    word-spacing: 8px;
  }
  .footer {
    display: none;
  }
  .image {
    display: none;
  }
  .button-wrap {
    width: 500px;
  }
  .button {
    width: 200px;
    height: 47px;
  }
}
@media only screen and (max-width: 480px) {
  .h2-wrapp h2 {
    letter-spacing: 4px;
  }
  .paragrag-wrap {
    width: 450px;
  }

  .button-wrap {
    margin-left: -20px;
  }
  .button {
    width: 240px;
    height: 56px;
  }
}
@media only screen and (max-width: 420px) {
  .paragraf {
    letter-spacing: 1.1;
    font-size: 2.3rem;
  }
}
</style>