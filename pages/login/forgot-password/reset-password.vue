<template>
  <body class="min-vw-100 min-vh-100 p-1">
    <div class="wrapp">
      <div class="container ml-5 mt-2">
        <nuxt-link to="/landing-page">
          <h1 class="header-title">Survey.In</h1>
        </nuxt-link>
      </div>

      <div class="container login-form mx-auto">
        <form method="post">
          <h2 class="header-login">Password Reset</h2>
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
              <div class="notif-text">
                <p class="p1">We send you a verification code to your email</p>
              </div>
              <input
                type="text"
                placeholder="Enter the verification code"
                name="uname"
                required
              />
              <div class="wrapp-button-login">
                <nuxt-link to="/new-password">
                  <button type="submit" class="button-login">
                    Request Password Reset
                  </button>
                </nuxt-link>
              </div>
              <div class="notif-text">
                <p class="p2">
                  Didn’t receive your verification code?
                  <span> Resend code</span>
                </p>
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
  top: 9.5%;
}
form {
  position: relative;
  top: 100px;
  background: white;
  border-radius: 20px;
  height: 260px;
}

.wrapp-input {
  position: relative;
  top: 0;
  padding: 30px;
}
p {
  font-size: 14px;
}
label {
  margin: 12px 0;
}
input[type='text'],
input[type='password'] {
  position: relative;
  top: -14px;
  width: 100%;
  padding: 9px 20px;
  margin: -20px 0;
  display: inline-block;
  border: 1px solid #ccc;
  box-sizing: border-box;
  border-radius: 18px;
}

.wrapp-button-login {
  position: relative;
  top: 8.5px;
  margin-top: -20px;
  left: 10%;
}
.button-login {
  position: relative;
  top: 9px;
  background-color: #009ee2;
  color: white;
  padding: 4px 20px;
  margin-top: 7px;
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
.notif-text {
  position: relative;
  top: -18px;
}
.p1 {
  position: relative;
  right: 10px;
  width: 300px;
}
.p2 {
  width: 100%;
  position: absolute;
  top: 45px;
  left: 14px;
}
span {
  cursor: pointer;
  position: relative;
  left: 28%;
  color: #009ee2;
}
@media (max-width: 576px) {
  .login-form {
    margin-left: 18%;
  }
}
</style>