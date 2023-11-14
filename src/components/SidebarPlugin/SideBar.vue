<template>
  <div class="sidebar"
       :style="sidebarStyle"
       :data-color="backgroundColor"
       :data-image="backgroundImage">
    <div class="sidebar-wrapper">
      <div class="logo">
        <a href="/" class="simple-text logo__container">
            <div class="logo-img">
                <img src="img/vue-logo.png" alt="">
            </div>
          {{title}}
        </a>
      </div>

      <slot name="content"></slot>
      <ul class="nav nav-main__links">
        <!--By default vue-router adds an active class to each route link. This way the links are colored when clicked-->
        <slot>
          <sidebar-link v-for="(link,index) in sidebarLinks"
                        :key="link.name + index"
                        :to="link.path"
                        @click="closeNavbar"
                        :link="link">
            <i :class="link.icon"></i>
            <p>{{link.name}}</p>
          </sidebar-link>
        </slot>
      </ul>
      <ul class="nav nav-bottom" v-if="$slots['bottom-links']">
        <slot name="bottom-links"></slot>
      </ul>
    </div>
    <div class="fixed-plugin">
    <div class="dropdown show-dropdown">
        <a data-toggle="dropdown">
            <i class="fa fa-cog fa-2x"></i>
        </a>
        <ul class="dropdown-menu">
            <li class="adjustments-line">
                <a href="#" class="switch-trigger centered-row">
                    <p>Background Image</p>
                    <div
                        class="bootstrap-switch bootstrap-switch-wrapper bootstrap-switch-animate bootstrap-switch-on">
                        <div class="bootstrap-switch-container">
                            <span class="bootstrap-switch-handle-on  bootstrap-switch-">
                                ON
                            </span>
                            <span class="bootstrap-switch-label"></span>
                            <span class="bootstrap-switch-handle-off bootstrap-switch-default">
                                OFF
                            </span>
                        </div>
                    </div>
                </a>
            </li>
            <li class="adjustments-line">
                <a href="#" class="switch-trigger centered-row">
                    <p>Sidebar Mini</p>
                    <div
                        class="bootstrap-switch bootstrap-switch-wrapper bootstrap-switch-animate bootstrap-switch-off">
                        <div class="bootstrap-switch-container">
                            <span class="bootstrap-switch-handle-on  bootstrap-switch-">
                                ON
                            </span>
                            <span class="bootstrap-switch-label"></span>
                            <span class="bootstrap-switch-handle-off bootstrap-switch-default">
                                OFF
                            </span>
                        </div>
                    </div>
                </a>
            </li>
            <li class="adjustments-line text-center">
                <a class="switch-trigger background-color">
                    <p>Filters</p>
                    <div class="pull-right centered-row">
                        <span data-color="black" class="badge filter badge-black active"></span>
                        <span data-color="azure" class="badge filter badge-azure"></span>
                        <span data-color="green" class="badge filter badge-green"></span>
                        <span data-color="blue" class="badge filter badge-blue"></span>
                        <span data-color="orange" class="badge filter badge-orange"></span>
                        <span data-color="red" class="badge filter badge-red"></span>
                        <span data-color="purple" class="badge filter badge-purple"></span>
                    </div>
                    <div class="clearfix"></div>
                </a>
            </li>
            <li class="header-title">Sidebar Images</li>
            <li class="">
                <a class="img-holder switch-trigger dropdown-item">
                    <img src="static/img/sidebar-1.jpg" alt="..."></a>
                </li>
                <li class="">
                    <a class="img-holder switch-trigger dropdown-item">
                        <img src="static/img/sidebar-3.jpg" alt="..."></a>
                    </li>
                    <li class="">
                        <a class="img-holder switch-trigger dropdown-item">
                            <img src="static/img/sidebar-4.jpg" alt="..."></a>
                        </li>
                        <li class="active">
                            <a class="img-holder switch-trigger dropdown-item">
                                <img src="static/img/sidebar-5.jpg" alt="..."></a>
                            </li>
                            <li class="button-container">
                                <div>
                                    <a
                                        href="https://www.creative-tim.com/product/vue-light-bootstrap-dashboard"
                                        target="_blank"
                                        class="btn btn-info btn-block btn-fill">Get Free Demo</a>
                                </div>
                            </li>
                            <li class="button-container">
                                <div>
                                    <a
                                        href="https://www.creative-tim.com/product/vue-light-bootstrap-dashboard-pro"
                                        target="_blank"
                                        class="btn btn-danger btn-block btn-fill">Buy for $49</a>
                                </div>
                            </li>
                            <li class="button-container">
                                <div>
                                    <a
                                        href="http://demos.creative-tim.com/vue-light-bootstrap-dashboard-pro/documentation/#/getting-started"
                                        target="_blank"
                                        class="btn btn-default btn-block">Documentation</a>
                                </div>
                            </li>
                            <li class="header-title d-flex justify-content-center">Thank you for sharing!</li>
                            <li class="button-container text-center">
                                <a href="javascript:void(0)" class="share-network-facebook">
                                    <button class="btn btn-facebook btn-icon">
                                        <i class="fa fa-fw fa-facebook"></i>
                                    </button>
                                </a>
                                <a href="javascript:void(0)" class="share-network-twitter">
                                    <button class="btn btn-twitter btn-icon">
                                        <i class="fa fa-fw fa-twitter"></i>
                                    </button>
                                </a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
</template>
<script>
  import SidebarLink from './SidebarLink.vue'

  export default {
    components: {
      SidebarLink
    },
    props: {
      title: {
        type: String,
        default: '유 & 안 세무회계'
      },
      backgroundColor: {
        type: String,
        default: 'black',
        validator: (value) => {
          let acceptedValues = ['', 'blue', 'azure', 'green', 'orange', 'red', 'purple', 'black']
          return acceptedValues.indexOf(value) !== -1
        }
      },
      backgroundImage: {
        type: String,
        default: 'img/sidebar-5.jpg'
      },
      activeColor: {
        type: String,
        default: 'success',
        validator: (value) => {
          let acceptedValues = ['primary', 'info', 'success', 'warning', 'danger']
          return acceptedValues.indexOf(value) !== -1
        }
      },
      sidebarLinks: {
        type: Array,
        default: () => []
      },
      autoClose: {
        type: Boolean,
        default: true
      }
    },
    provide () {
      return {
        autoClose: this.autoClose
      }
    },
    computed: {
      sidebarStyle () {
        return {
          backgroundImage: `url(${this.backgroundImage})`
        }
      }
    },
    methods: {
      
    }
  }

</script>
<style>
  .sidebar .sidebar-wrapper {
    display: flex;
    flex-direction: column;
  }
 .sidebar .nav-main__links {
   flex: 1;
 }
 .sidebar .sidebar-wrapper .logo .logo__container {
   padding-left: 10px;
 }
</style>
