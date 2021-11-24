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
            <div class="button-wrap d-flex align-items-center">
              <b-button class="button" id="show-btn" @click="showModal"
                ><img
                  src="~/assets/image/plusButtoon.svg"
                  alt=""
                  class="mr-1"
                />
                Join Survey Group</b-button
              >
              <b-modal
                ref="my-modal"
                hide-footer
                hide-header
                style="background-color: #009ee2; border-radius: 0 0 40px 40px"
              >
                <h4
                  class="text-center fw-normal"
                  style="font-weight: 300; padding: 5px; margin-bottom: 15px"
                >
                  Insert code here given by admin or survey creator to join a
                  survey group
                </h4>
                <input
                  type=""
                  name=""
                  value=""
                  placeholder="Insert survey group code"
                />
                <b-button
                  class="button button-join mt-3 mx-auto"
                  block
                  @click="toggleModal"
                  >Join</b-button
                >
              </b-modal>
              <div>
                <b-button v-b-modal.modal-1 class="button"
                  ><img
                    src="~/assets/image/twoPersonIcon.svg"
                    alt=""
                    class="mr-2"
                  />
                  Create Group</b-button
                >

                <b-modal hide-footer hide-header id="modal-1">
                  <h2 class="text-center mb-3">Create new survey group</h2>
                  <form @submit="onSubmit" action="" hide-footer>
                    <label for="fname">Group name</label>
                    <input
                      type="text"
                      id="fname"
                      name="firstname"
                      placeholder="Your name.."
                      v-model="group_name"
                    />

                    <label for="lname">Group description</label>
                    <textarea
                      id="w3review"
                      name="w3review"
                      cols="57"
                      style="border-radius: 20px"
                      placeholder="Group Description"
                      v-model="group_desc"
                    >
                    </textarea>
                    <label for="lname">Group Token</label>
                    <input
                      type="text"
                      id="lname"
                      name="lastname"
                      placeholder="Your last name.."
                      v-model="token"
                    />
                    <!-- <label id="file" for="file">Group Image</label>
                    <input
                      type="file"
                      id="lname"
                      class=""
                      accept="image/*"
                      @change="onFileChange"
                    /> -->
                    <br /><br />
                    <div class="container-fluid d-flex justify-content-center">
                      <div class="col-12">
                        <button class="button-create center" type="submit">
                          Create
                        </button>
                      </div>
                    </div>
                  </form>
                </b-modal>
              </div>
            </div>

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
              <b-dropdown-item href="#" class="text-center mt-3"
                >My Account</b-dropdown-item
              >
              <b-dropdown-item href="#" class="text-center text-item"
                >Sign Out</b-dropdown-item
              >
            </b-nav-item-dropdown>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      group: [],

      group_name: '',
      group_desc: '',
      group_pict: '',
      token: '',
      created_at: '',
      updated_at: '',
    }
  },

  methods: {
    onSubmit(e) {
      e.preventDefault()
      console.log(this.onFileChange())
      const newGroup = {
        group_name: this.group_name,
        group_desc: this.group_desc,
        token: this.token,
        // group_pict: this.onFileChange(),
      }

      this.$emit('add-group', newGroup)

      this.group_name = ''
      this.group_desc = ''
      this.token = ''
      // this.group_pict = ''
    },

    // onFileChange(event) {
    //   this.group_pict = event.target.files[0].name
    //   console.log(this.group_pict)
    // },
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

b-modal {
  -webkit-border-radius: 40px !important;
  -moz-border-radius: 40px !important;
  border-radius: 40px !important;
}
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
textarea {
  border: 1px solid rgb(168, 60, 60);
  box-shadow: 2px 2px 3px rgb(61, 58, 58);
  border-radius: 10px;
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
  width: 100%;
  border: 1px solid rgb(199, 192, 192);
  box-shadow: 2px 2px 3px rgb(61, 58, 58);
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
input[type='file'] {
  text-align: center;
  width: 100%;
  padding: 10px;
  margin: 4px 0;
  color: #f3f3f3;
  background: url('assets/icon/left-arrow.png');
  background: #75b54a;
}
::-webkit-file-upload-button {
  width: 37.5%;
  visibility: hidden;
}

.button-create {
  width: 170px;
  height: 40px;
  background-color: #009ee2;
  color: aliceblue;
  border-radius: 10px;
  border: 1px solid;
  font-weight: 500;
  font-size: 1.2rem;
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