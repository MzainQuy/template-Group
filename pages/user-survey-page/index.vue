<template>
  <body class="min-vw-100 min-vh-100">
    <navbar-group />
    <div class="container-fluid">
      <div class="container">
        <div class="hero-image">
          <div class="hero-text p-3 ml-4">
            <h2>Survey group 1</h2>
            <div>
              <span
                >Lorem ipsum dolor sit amet, consectetur adipiscing elit.
              </span>
            </div>
            <div>
              <span>Arnold Dixon - (Owner)</span>
            </div>
            <div>
              <span>10 members</span>
            </div>
            <div class="button-wrapp">
              <button type="" class="button">
                <img src="~assets/image/exitIcon.svg" alt="" /> Exit group
              </button>
            </div>
          </div>
        </div>
      </div>
      <div class="container">
        <div class="row">
          <div class="col-lg-2 text-center mt-2">
            <div class="button-wrapp">
              <button
                @click="component = 'amount-User'"
                type=""
                class="button-members"
              >
                <div class="mr-1">
                  <img src="~assets/image/surveyIcon.svg" alt="" class="mr-1" />
                  Members
                </div>
              </button>
              <button
                @click="component = 'survey-User'"
                type=""
                class="button-survey"
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
import amountUser from '~/components/amountUser.vue'
import surveyUser from '~/components/surveyUser.vue'

export default {
  components: {
    'amount-User': amountUser,
    'survey-User': surveyUser,
  },
  data() {
    return {
      component: 'amount-User',
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
  border: none;
  width: 140px;
  border-radius: 10px;
  background-color: #f0500f;
  color: azure;
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