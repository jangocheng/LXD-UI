<template>
  <div>
    <!-- Main header -->
    <main-header :current="$route.path"></main-header>

    <!-- Main element -->
    <el-main>
      <div class="columns">
        <div class="column is-narrow">
          <side-menu></side-menu>
        </div>
        <div class="column">
          <h6 class="title is-6">Empty Page</h6>

          <div class="box">
            <div class="card-content">
              <p>This is an empty page with side menu.</p>
            </div>
          </div>
        </div>
      </div>
    </el-main>
  </div>
</template>

<script>
  import MainHeader from './Layout/MainHeader'
  import SideMenu from './Layout/SideMenu'

  export default {
    name: 'empty-page',
    components: { MainHeader, SideMenu },
    mixins: [],
    data () {
      return {}
    },
    mounted: function () {},
    methods: {
      open (link) {
        this.$electron.shell.openExternal(link)
      }
    }
  }
</script>

<style scoped>

</style>