// TEMPLATE MARKUP
<template>
  <div id="app">
    <div class="nav has-shadow">
      <div class="container">
        <div class="nav-left">
          <a href="#" class="nav-item"><img src="./assets/logo.png"></a>
        </div>

        <span class="nav-toggle" v-on:click="toggleNav" v-bind:class="{ 'is-active': isActive }">
          <span></span>
          <span></span>
          <span></span>
        </span>

        <div class="nav-right nav-menu" v-bind:class="{ 'is-active': isActive }">
          <router-link to="/" class="nav-item r-item">Home</router-link>
          <router-link to="/" class="nav-item r-item">About</router-link>
          <router-link to="/" class="nav-item r-item">Features</router-link>
          <router-link to="faq" class="nav-item r-item">FAQ</router-link>

          <div class="nav-item">
            <p class="control">
              <a href="" class="button is-primary is-outlined">
                <span class="icon">
                  <i class="fa fa-download"></i>
                </span>
                <span>Download</span>
              </a>
            </p>
          </div>
        </div>
      </div>
    </div>
    <router-view></router-view>
    <footer class="footer is-primary">
      <div class="container">
        <div class="columns">
          <div class="column">
            <p>&copy;2017 ALL RIGHTS RESERVED</p>
          </div>
          <div class="column has-text-right">
            <a href="#" class="icon"><i class="fa fa-twitter"></i></a>
            <a href="#" class="icon"><i class="fa fa-linkedin"></i></a>
            <a href="#" class="icon"><i class="fa fa-instagram"></i></a>
            <a href="#" class="icon"><i class="fa fa-facebook"></i></a>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

// SCRIPTS & LOGIC
<script>
export default {
  name: 'app',
  data: function() {
    return {
      isActive: false
    }
  },
  methods: {
    toggleNav: function() {
      this.isActive = !this.isActive;
    }
  }
}
</script>

// COMPONENT STYLES
<style lang="sass">
@import '../node_modules/bulma/bulma.sass'
@import 'breakpoints'

.nav  
  background-color: #383838
  a:hover
    color: gray

a.r-item
  color: #C1C1C1
  padding: .5rem 1.5rem
  +mobile
    color: gray
    &:hover
      background-color: #F1F1F1

.nav-toggle span 
  background-color: #C1C1C1

footer
  background-color: $primary !important
  color: #fff
  .icon
    color: #fff
    margin-left: 1.2em

</style>
