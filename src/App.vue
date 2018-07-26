<template>
  <div id="app">
    <resize-observer @notify="handleResize" />
    <div class="wrapper">
        <div class="sidebar collapse show" id="sidebar" data-background-color="white" data-active-color="danger">
        	<div class="sidebar-wrapper">
                <div class="logo">
                    <a href="/" class="simple-text">
                        Anisha Keshavan
                    </a>
                </div>

                <ul class="nav">

                  <router-link to="/" tag="li" exact>
                    <a>
                      <i class="ti-user"></i>
                      <p>About Me</p>
                    </a>
                  </router-link>

                  <router-link to="/projects" tag="li" exact>
                    <a>
                      <i class="ti-thought"></i>
                      <p>Projects</p>
                    </a>
                  </router-link>

                  <router-link to="/teaching" tag="li" exact>
                    <a>
                      <i class="ti-pencil"></i>
                      <p>Teaching</p>
                    </a>
                  </router-link>


                  <router-link to="/publications" tag="li" exact>
                    <a>
                      <i class="ti-announcement"></i>
                      <p>Publications</p>
                    </a>
                  </router-link>

                  <router-link to="/cv" tag="li" exact>
                    <a>
                      <i class="ti-clipboard"></i>
                      <p>CV</p>
                    </a>
                  </router-link>


                </ul>
        	</div>
        </div>

        <div class="main-panel" id="main-panel">

          <nav class="navbar navbar-default">
            <div class="container-fluid">
                <div class="navbar-header">
                    <button type="button" class="btn btn-secondary btn-small"
                    id="toggleBtn"
                     @click="toggleNav">
                        <!--<span class="sr-only">Toggle navigation</span>
                        <span class="icon-bar bar1"></span>
                        <span class="icon-bar bar2"></span>
                        <span class="icon-bar bar3"></span>-->
                        <span v-if="sidebarOpen"> <i class="ti-close"></i> </span>
                        <span v-else> <i class="ti-menu"></i> </span>
                    </button>
                    <a class="simple-text routename mr-3">{{routeName}}</a>
                    <form class="form-inline" style="display: inline;" v-if="routeName=='Projects'">
                      <input id="searchProject" class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
                      <!--<button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>-->
                    </form>
                </div>
            </div>
        </nav>
        <transition name="slide-fade" mode="out-in">
          <router-view></router-view>
        </transition>
        </div>
    </div>


  </div>
</template>

<script>
import Vue from 'vue'
import VueResize from 'vue-resize'

Vue.use(VueResize)

//require('../node_modules/boostrap/dist/css/bootstrap-grid.min.css');
//const $ = require('jquery');
require('../node_modules/bootstrap/dist/css/bootstrap.min.css');
require('./assets/css/demo.css');
require('./assets/css/paper-dashboard.css');
require('./assets/css/themify-icons.css');
require('./assets/css/animate.min.css');

export default {
  name: 'App',
  data() {
    return {
      sidebarOpen: true,
    }
  },
  computed: {
    routeName() {
      return this.$route.name
    }
  },
  mounted() {
    if (window.innerWidth >= 991) {
      this.sidebarOpen = true;
    } else {
      this.sidebarOpen = false;
    }
  },
  watch: {
    $route(to, from) {
      if (window.innerWidth < 991) {
        this.hideSidebar()
      } else {
        this.showSidebar();
      }
    },
  },
  methods: {

    hideSidebar() {
      document.getElementById("sidebar").style.width="0px";
      document.getElementById("sidebar").className = "sidebar"
      document.getElementById("main-panel").style.left='0';
      document.getElementById("main-panel").className = "main-panel"
      this.sidebarOpen = false;
    },

    showSidebar() {
      document.getElementById("sidebar").style.width=null;
      document.getElementById("sidebar").className = "sidebar expand"
      document.getElementById("main-panel").style.left= window.innerWidth >= 991 ? "0px" : "260px";
      document.getElementById("main-panel").className = "main-panel expand"
      this.sidebarOpen = true;
    },

    handleResize() {
      if (window.innerWidth >= 991) {
        this.showSidebar();
      }
      if (window.innerWidth < 991) {
        this.hideSidebar();
      }
    },

    toggleNav() {
      const sidebarIsNull = document.getElementById("sidebar").style.width == null;
      const sidebarIs0 = document.getElementById("sidebar").style.width == "0px"
      const sidebarHasExpand = document.getElementById("sidebar").className.indexOf('expand') >= 0;
      // toggle the navbar here
      if (sidebarIsNull){
        console.log("sidebar is null")
        this.hideSidebar();
      }

      if (!sidebarIs0){
        console.log("sidebar is 0")
        this.hideSidebar();
      }

      if (!sidebarHasExpand){
        console.log("showing")
        this.showSidebar();
      }

    }
  }
};
</script>

<style>

.nav {
  display: block !important;
}

.nav>li {
  position: relative;
  display: block;
  margin-top: 35px;
  margin-bottom: 35px;
}

li a {
  display: inherit;
  margin-top: 25px;
  margin-bottom: 25px;
}

.sidebar .nav li > a {
  padding-top: 12.5px;
  padding-bottom: 12.5px;
}

.navbar {
  padding: 0 !important;
  margin: 0 !important;
}

.routename {
  font-size: 1.5em;
  font-weight: 100;
}

/* Enter and leave animations can use different */
/* durations and timing functions.              */
.slide-fade-enter-active {
  transition: all .2s ease;
}
.slide-fade-leave-active {
  transition: all .2s cubic-bezier(1.0, 0.5, 0.8, 1.0);
}
.slide-fade-enter, .slide-fade-leave-to
/* .slide-fade-leave-active below version 2.1.8 */ {
  transform: translateX(10px);
  opacity: 0;
}

/*#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}*/
</style>
