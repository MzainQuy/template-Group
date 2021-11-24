<template>
  <body class="min-vw-100 min-vh-100 position-relative">
    <div class="container-fluid content">
      <navbar @add-group="addGroup" />
      <!-- <firstLoginImg /> -->
      <CardUserGroup :group="Group" />
    </div>
  </body>
</template>

<script>
import CardUserGroup from '~/components/cardUserGroup.vue'

export default {
  name: 'pageUser',
  components: { CardUserGroup },
  data() {
    return {
      show: false,
      Group: [],
    }
  },
  methods: {
    async showGroup() {
      const res = await fetch('http://localhost:8000/api/group')
      const data = await res.json()
      return data
    },

    async addGroup(task) {
      const res = await fetch('http://localhost:8000/api/group/create', {
        method: 'POST',
        headers: {
          'Content-type': 'application/json',
        },
        body: JSON.stringify(task),
      })

      const data = await res.json()

      this.Group = data
      console.log(task)
    },
  },

  async created() {
    this.Group = await this.showGroup()
  },
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,900;1,300;1,500&display=swap');

body {
  margin: 0;
  padding: 0;
  background-color: #c8edff;
}
</style>