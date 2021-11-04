<template>
  <html>
    <body class="min-vw-100 min-vh-100 p-1">
      <div class="container-fluid position-relative">
        <div class="ml-5 mt-2 header-title">
          <nuxt-link to="/">
            <h1 class="header-title">Survey.In</h1>
          </nuxt-link>
        </div>
        <div class="container login-form mt-5 mx-auto">
          <form method="post">
            <h2 class="header-login">Login</h2>

            <div class="container">
              <div class="wrapp-input">
                <label for="uname"><b>Email</b></label>
                <input
                  type="text"
                  placeholder="Enter Email"
                  name="uname"
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
                  <nuxt-link to="/page-user">
                    <button type="submit" class="button-login">Login</button>
                  </nuxt-link>
                </div>
                <div class="use-account">
                  <span class="">Or use your account</span>
                </div>
                <div class="icon-wrapp text-center">
                  <div class="icon">
                    <img src="~assets/icon/google.png" alt="" class="logo" />
                  </div>
                  <div class="icon">
                    <img src="~assets/icon/facebook.png" alt="" class="logo" />
                  </div>
                </div>
                <div class="wrapp-password">
                  <span class="">
                    Forgot your
                    <nuxt-link to="login/forgot-password">password?</nuxt-link>
                  </span>
                </div>
              </div>
            </div>
          </form>
        </div>
      </div>
    </body>
  </html>
</template>

<script>
export default {}
</script>

<style scoped>
body {
  background-color: #c8edff;
}

.header-title {
  font-family: 'Roboto', sans-serif;
  color: #009ee2;
  font-size: 37px;
}
.login-form {
  margin-top: 30px;
  max-width: 450px;
  max-height: 540px;
}
.header-login {
  position: relative;
  width: 0;
  left: 40%;
  top: 7.5%;
}
form {
  background: white;
  border-radius: 27px;
  height: 540px;
}

.wrapp-input {
  position: relative;
  top: 8px;
  padding: 30px;
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
.use-account {
  position: relative;
  left: 24%;
  top: 14px;
  margin: 20px 0;
}

.icon-wrapp {
  cursor: pointer;
  position: relative;
  left: 27%;
  display: flex;
  width: 0;
}
.icon {
  margin: 18px 12px;
}
.logo {
  width: 40px;
}

.wrapp-password {
  position: relative;
  left: 21.1%;
  top: 0;
}
/* 
@media (max-width: 576px) {
  .header-title {
    margin-top: -0.5rem;
    margin-left: -2rem;
    font-size: 50px;
  }
  .login-form {
    position: relative;
    left: 23px;
    margin-top: 29px;
  }
} */
</style>