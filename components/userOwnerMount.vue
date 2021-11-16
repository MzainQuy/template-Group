<template>
  <div class="Surveys col-lg-10 col-md-12 mt-3 mx-auto">
    <div class="list-survey">
      <ul>
        <li>
          <div class="d-flex justify-content-between align-items-center">
            <a href="" class="mr-auto p-3">Name</a>
            <a href="" class="ml-3 mr-auto p-3">Role</a>
            <button type="" class="button-invite">
              <img src="~assets/image/personIcon.svg" alt="" class="" />Invite
              members
            </button>
          </div>
        </li>
      </ul>
    </div>

    <div class="list-survey">
      <ul>
        <li>
          <div
            class="
              d-flex
              justify-content-between
              align-items-center
              position-relative
            "
          >
            <div class="name-list">
              <img
                src="~/assets/icon/card-img1.jpg"
                alt=""
                class="ml-3 mt-1 img-user"
              />
              <a href="" class="member-list ml-1">Jonh marchel sdada</a>
            </div>
            <a href="" class="role-user">Member</a>
            <button type="" class="button-invite action">Invite members</button>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.list-survey {
  width: 100%;
}

.list-survey ul li {
  border-radius: 12px;
  list-style-type: none;
  height: 60px;
  background-color: white;
}
.list-survey ul li a {
  font-weight: bold;
  color: #222830;
}
.button-invite {
  color: aliceblue;
  position: relative;
  top: 3px;
  left: -10px;
  box-sizing: border-box;
  border: none;
  border-radius: 5px;
  width: 170px;
  height: 35px;
  background-color: #75b54a;
}

.button-invite.action {
  background-color: #222831;
}
.list-survey .img-user {
  position: relative;
  top: 3px;
  left: -10px;
  border-radius: 50%;
  width: 48px;
  height: 48px;
}
.name-list {
  min-width: 200px;
}
.member-list {
  position: relative;
  top: 3px;
  left: -10px;
}
.role-user {
  position: absolute;
  left: 44%;
}
</style>