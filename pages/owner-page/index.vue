<template>
  <body class="min-vw-100 min-vh-100">
    <navbar-group />
    <div class="container-fluid">
      <div class="container-fluid">
        <div class="hero-image">
          <div class="hero-text p-3 ml-3">
            <h2>Survey group 1</h2>
            <div>
              <span
                >Lorem ipsum dolor sit amet, consectetur adipiscing elit.
              </span>
            </div>
            <div class="d-flex">
              <span class="mr-auto">Arnold Dixon - (Owner)</span>
            </div>
            <div class="d-flex">
              <span class="mr-auto">10 members</span>
              <div class="">
                <button type="" class="button d-block">
                  <img src="~assets/image/mountain-icon.svg" alt="" /> Change
                  image banner
                </button>
                <button type="" class="button d-block button-c">
                  <img src="~assets/image/pencil.svg" alt="" /> Edit group
                  information
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="container-fluid">
        <div class="row">
          <div class="col-lg text-center mt-2">
            <div class="button-wrapp">
              <button
                @click="component = 'amount-Owner'"
                type=""
                class="button-members"
              >
                <div class="mr-1">
                  <img src="~assets/image/surveyIcon.svg" alt="" class="mr-1" />
                  Members
                </div>
              </button>
              <button
                type=""
                class="button-survey"
                @click="component = 'survey-Owner'"
              >
                <div class="mr-2">
                  <img
                    src="~assets/image/membersIcon.svg"
                    alt=""
                    class="mr-2"
                  />Surveys
                </div>
              </button>
            </div>
          </div>
          <component :is="component"></component>
        </div>
      </div>
    </div>
  </body>
</template>

<script>
import userOwnerMount from '~/components/userOwnerMount.vue'
import surveyOwner from '~/components/surveyOwner.vue'

export default {
  components: {
    'amount-Owner': userOwnerMount,
    'survey-Owner': surveyOwner,
  },
  data() {
    return {
      component: 'amount-Owner',
    }
  },
}
</script>

<style scoped>
body {
  background-color: #c8edff;
}

.hero-image {
  border-radius: 19px;
  margin-top: 8px;
  background-image: url('~/assets/icon/card-img1.jpg');
  height: 22vh;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
}
.hero-text {
  color: beige;
}
.button-wrapp {
  margin-top: 10px;
}
.button {
  position: relative;
  top: -25px;
  border: none;
  width: 220px;
  padding: 4px;
  border-radius: 10px;
  background-color: #c4c4c4;
  color: azure;
  margin-top: 10px;
}
.button.button-c {
  background-color: #009ee2;
}
.button-survey {
  border: none;
  width: 220px;
  height: 35px;
  border-radius: 0px 0px 8px 8px;
  background-color: #fff;
}
.button-members {
  border: none;
  width: 220px;
  height: 35px;
  border-radius: 8px 8px 0px 0px;

  color: #ffffff;
  background-color: #222830;
}

.list-survey {
  width: 100%;
}

.list-survey ul li {
  border-radius: 12px;
  list-style-type: none;
  height: 75px;
  background-color: white;
}
.list-survey ul li a {
  /* margin-top: 22px; */
  font-weight: bold;
  color: #222830;
}
.list-survey img {
  border-radius: 50%;
  /* margin-left: 10px; */
  width: 60px;
  height: 60px;
  /* margin-top: 5px; */
}
</style>