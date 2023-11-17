<template>
  <div class="wrapper">
    <side-bar>
      <mobile-menu slot="content"></mobile-menu>
      <sidebar-link to="/admin/overview">
        <i class="nc-icon nc-chart-pie-35"></i>
        <p>대시보드</p>
      </sidebar-link>
      <sidebar-link to="/admin/user">
        <i class="nc-icon nc-circle-09"></i>
        <p>프로필</p>
      </sidebar-link>
      <sidebar-link to="/admin/annual-list">
        <i class="nc-icon nc-notes"></i>
        <p>연차</p>
      </sidebar-link>
      <sidebar-link to="/admin/notifications">
        <i class="nc-icon nc-bell-55"></i>
        <p>공지사항</p>
      </sidebar-link>
      <sidebar-link to="/admin/calendar">
        <i class="nc-icon nc-single-copy-04"></i>
        <p>캘린더</p>
      </sidebar-link>

      <template slot="bottom-links">
        <sidebar-link class="active"
                      to="/admin/upgrade">
          <i class="nc-icon nc-alien-33"></i>
          <p>Upgrade to PRO</p>
        </sidebar-link>
      </template>
    </side-bar>
    <div class="main-panel">
      <top-navbar></top-navbar>

      <dashboard-content @click="toggleSidebar">

      </dashboard-content>

      <content-footer></content-footer>  
    </div>
  </div>
</template>
<style lang="scss">

</style>
<script>
  import TopNavbar from './TopNavbar.vue'
  import ContentFooter from './ContentFooter.vue'
  import DashboardContent from './Content.vue'
  import MobileMenu from './MobileMenu.vue'
  export default {
    components: {
      TopNavbar,
      ContentFooter,
      DashboardContent,
      MobileMenu
    },
    methods: {
      toggleSidebar () {
        if (this.$sidebar.showSidebar) {
          this.$sidebar.displaySidebar(false)
        }
      }
    }
  }

</script>
