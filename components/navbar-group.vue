<template>
  <div class="container-fluid sticky-top">
    <div
      class="container-fluid sticky-top"
      style="background-color: #009ee2; border-radius: 0 0 40px 40px"
    >
      <b-navbar toggleable="lg" type="dark" variant="">
        <b-navbar-brand href="/" class="header-title">Survey.In</b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto">
            <b-nav-item-dropdown right class="profile-toggle">
              <!-- Using 'button-content' slot -->
              <template #button-content>
                <img src="~assets/icon/card-img4.jpg" />
              </template>
              <div class="container-fluid">
                <div class="col-2 mr-5 mt-2">
                  <span>username</span>
                  <span>username@gmail.com</span>
                </div>
                <div class="col-2 img-profile mr-3 mt-3">
                  <img src="~assets/icon/card-img4.jpg" />
                </div>
              </div>
              <span class="text-account">
                <b-dropdown-item href="#" class="text-center mt-3"
                  >My Account</b-dropdown-item
                >
              </span>
              <span class="text-account">
                <b-dropdown-item href="#" class="text-center"
                  >Sign Out</b-dropdown-item
                >
              </span>
            </b-nav-item-dropdown>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    showModal() {
      this.$refs['my-modal'].show()
    },
    hideModal() {
      this.$refs['my-modal'].hide()
    },
    toggleModal() {
      // We pass the ID of the button that we want to return focus to
      // when the modal has hidden
      this.$refs['my-modal'].toggle('#toggle-btn')
    },
  },
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,900;1,300;1,500&display=swap');

.header-title {
  font-family: 'Roboto', sans-serif;
  color: #fff;
  font-size: 37px;
}

.button {
  margin-right: 18px;
  width: 190px;
  height: 37px;
  background-color: #75b54a;
  color: aliceblue;
  border-radius: 10px;
  border: 0 solid;
}

.dropdown img {
  border-radius: 50%;
  background-position: center;
  width: 40px;
  height: 40px;
}
b-modal {
  text-align: center;
}
input {
  text-align: center;
  width: 100%;
  border: 3px solid #364e24;
  border-radius: 10px;
}

label {
  margin: 12px 0;
}
input[type='text'],
input[type='password'] {
  width: 100%;
  padding: 10px;
  margin: 4px 0;
  display: inline-block;
  border: 1px solid rgb(139, 33, 33);
  box-sizing: border-box;
  border-radius: 18px;
}

@media only screen and (max-width: 998px) {
  .button-wrap {
    margin-top: 20px;
    display: flex;
    justify-content: right;
    flex-direction: row;
  }
  .profile-toggle {
    display: flex;
    flex-wrap: wrap;
    margin-top: -50px;
  }
}
@media only screen and (max-width: 600px) {
  .button {
    width: 130px;
    height: 45px;
    font-size: 13px;
    margin-top: 15px;
  }
  .button-wrap {
    margin-top: -4px;
    display: flex;
    justify-content: center;
  }
  .profile-toggle {
    display: flex;
    justify-content: center;
    display: flex;
    flex-wrap: wrap;
    margin-top: 8px;
  }
}
</style>