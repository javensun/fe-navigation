<template>
  <div class="container">
    <router-view />
    <SideBar v-if="isShowSideBar" />
  </div>
</template>

<script>
import SideBar from './SideBar'
export default {
  data () {
    return {
      isShowSideBar: true
    }
  },
  mounted () {
    this.isShowSideBar = this.$route.name !== 'experiment'
  },
  components: {
    SideBar
  }
}
</script>

<style lang="scss">
.container {
  display: flex;
  width: 100%;
}
</style>
