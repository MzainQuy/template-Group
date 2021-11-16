<template>
  <html>
    <body class="min-vw-100 min-vh-100 p-1">
      <div class="container-fluid position-relative">
        <div class="ml-5 mt-2 header-title">
          <nuxt-link to="/">
            <h1 class="header-title">Survey.In</h1>
          </nuxt-link>
        </div>
        <div class="container regist-form mt-5 mx-auto">
          <form method="post">
            <h2 class="header-regis">Register</h2>

            <div class="container">
              <div class="wrapp-input">
                <label for="uname"><b>Name</b></label>
                <input
                  type="text"
                  placeholder="Enter Name"
                  name="uname"
                  required
                />
                <label for="psw"><b>Email</b></label>
                <input
                  type="email"
                  placeholder="Enter Email"
                  name="eml"
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
                    <button type="submit" class="button-login">Register</button>
                  </nuxt-link>
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
.regist-form {
  margin-top: 30px;
  max-width: 450px;
  max-height: 540px;
}
.header-regis {
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
  top: 8px;
  padding: 30px;
}

input[type='text'],
input[type='password'],
input[type='email'] {
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
</style>