<template>
  <body>
    <div class="wrapp">
      <div class="container ml-5 mt-2">
        <nuxt-link to="/landing-page">
          <h1 class="header-title">Survey.In</h1>
        </nuxt-link>
      </div>

      <div class="container login-form">
        <form method="post">
          <h2 class="header-login">Create new password</h2>
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
                placeholder="New Password"
                name="uname"
                required
              />
              <input
                type="text"
                placeholder="Confirm new password"
                name="uname"
                required
              />
              <div class="wrapp-button-login">
                <nuxt-link to="/login">
                  <button type="submit" class="button-login">
                    Reset Password
                  </button>
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
  margin-top: -10px;
  width: 100%;
  height: 1200px;
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
  left: 12%;
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
  padding: 40px;
}

label {
  margin: 12px 0;
}
input[type='text'],
input[type='password'] {
  position: relative;
  top: -14px;
  width: 100%;
  padding: 8px 20px;
  margin: 8px 0;
  display: inline-block;
  border: 1px solid #ccc;
  box-sizing: border-box;
  border-radius: 18px;
}

.wrapp-button-login {
  position: relative;
  top: 5px;
  left: 10%;
}
.button-login {
  position: relative;
  top: -10px;
  background-color: #009ee2;
  color: white;
  padding: 5px 20px;
  margin-top: 2px;
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
</style>