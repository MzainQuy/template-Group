<template>
  <body class="min-vw-100 min-vh-100 p-1">
    <div class="container-fluid">
      <div class="container ml-5 mt-2">
        <nuxt-link to="/landing-page">
          <h1 class="header-title">Survey.In</h1>
        </nuxt-link>
      </div>

      <div class="container login-form mx-auto">
        <form method="post">
          <h2 class="header-login">Forgot-Password</h2>
          <div class="container">
            <div class="arrow-icon">
              <nuxt-link to="/login">
                <img
                  src="~assets/icon/left-arrow.png"
                  alt=""
                  class="icon-arrow"
                />
              </nuxt-link>
            </div>
            <div class="wrapp-input">
              <input
                type="text"
                placeholder="Your E-mail"
                name="uname"
                required
              />
              <div class="wrapp-button-login">
                <nuxt-link to="forgot-password/reset-password">
                  <button class="button-login">Request Password Reset</button>
                </nuxt-link>
              </div>
            </div>
          </div>
        </form>
      </div>
    </div>
  </body>
</template>

<script>
export default {}
</script>

<style scoped>
body {
  background-color: #c8edff;
}

.container {
  padding: 16px;
}
.header-title {
  font-family: 'Roboto', sans-serif;
  color: #009ee2;
  font-size: 37px;
}
.login-form {
  position: relative;
  max-width: 400px;
  max-height: 260px;
}
.header-login {
  font-size: 28px;
  position: relative;
  left: 21.5%;
  top: 13.5%;
}
form {
  position: relative;
  top: 100px;
  background: white;
  border-radius: 27px;
  height: 260px;
}

.wrapp-input {
  position: relative;
  top: 0;
  padding: 30px;
}

label {
  margin: 12px 0;
}
input[type='text'],
input[type='password'] {
  width: 100%;
  padding: 12px 20px;
  margin: 8px 0;
  display: inline-block;
  border: 1px solid #ccc;
  box-sizing: border-box;
  border-radius: 18px;
}

.wrapp-button-login {
  position: relative;
  top: 15px;
  left: 10%;
}
.button-login {
  background-color: #009ee2;
  color: white;
  padding: 8px 20px;
  margin-top: 6px;
  border: none;
  cursor: pointer;
  width: 80%;
  border-radius: 20px;
}

.icon-arrow {
  width: 20px;
  position: absolute;
  top: 7%;
  margin: 0 10px;
}

@media (max-width: 576px) {
  .login-form {
    margin-left: 15%;
  }
}
</style>