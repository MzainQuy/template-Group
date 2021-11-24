<template>
  <body>
    <div class="container-fluid">
      <div class="row">
        <div class="col-12 position-relative text-center">
          <h1 class="header-class">Survey Groups</h1>
        </div>
        <div
          v-for="groupLop in group.Group"
          :key="groupLop.id"
          class="col-lg-3 col-md-6 mt-4"
        >
          <CardChild :groupChild="groupLop" />
        </div>
      </div>
    </div>
  </body>
</template>

<script>
import CardChild from '~/components/cardchild.vue'
export default {
  name: 'groupWrapper',
  components: { CardChild },
  props: {
    group: Array,
  },
}
</script>

<style scoped>
.header-class {
  position: relative;
  top: 20px;
}
</style>