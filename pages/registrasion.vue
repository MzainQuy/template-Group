<template>
  <body class="min-vw-100 min-vh-100 p-1">
    <div class="wrapp">
      <div class="container ml-5">
        <nuxt-link to="/">
          <h1 class="header-title">Survey.In</h1>
        </nuxt-link>
      </div>

      <div class="container login-form mt-3 mx-auto">
        <form method="post">
          <h2 class="header-login">Register</h2>

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
              <label for="uname"><b>Nama</b></label>
              <input
                type="text"
                placeholder="Enter UserName"
                name="uname"
                required
              />
              <label for="psw"><b>Email</b></label>
              <input
                type="password"
                placeholder="Enter Email"
                name="psw"
                required
              />
              <label for="psw"><b>Password</b></label>
              <input
                type="password"
                placeholder="Enter Password"
                name="psw"
                required
              />
              <div class="wrapp-button-login">
                <nuxt-link to="/login">
                  <button type="submit" class="button-login">Login</button>
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
  /* width: 100%; */
  /* height: 100vh; */
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
  max-width: 450px;
  max-height: 540px;
}
.header-login {
  position: relative;
  width: 0;
  left: 34%;
  top: 7.5%;
}
form {
  background: white;
  border-radius: 27px;
  height: 540px;
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
  left: 22%;
}
.button-login {
  background-color: #009ee2;
  color: white;
  padding: 8px 20px;
  margin-top: 6px;
  border: none;
  cursor: pointer;
  width: 50%;
  border-radius: 20px;
}

.icon-arrow {
  width: 20px;
  position: absolute;
  top: 17.4%;
  margin: 0 10px;
}
</style>