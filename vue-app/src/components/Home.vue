<template>
  <div class="home">
    <section class="hero">
      <div class="hero-body">
        <div class="container">
          <h1 class="title">{{ heading }}</h1>
          <div class="is-two-thirds column is-paddingless">
            <h2 class="subtitle is-4">{{ subheading }}</h2>
          </div>
          <a href="" class="button is-large is-primary" id="learn">Learn More</a>
        </div>
      </div>
    </section>

    <section class="section">
      <div class="container">
        <div class="columns pd is-desktop">
          <div class="column is-12 has-text-centered">
            <h2 class="body-heading">{{ bodyheading }}</h2>
            <p>Vue.js is super simple and minimal js framework that will allow you to build apps fast like never before! It's extremely lightweight and highly performant. This is a simple web structure that I created to get acustomed to the Vue way!</p>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'home',
  data() {
    return {
      heading: 'Vue.js Web Application',
      subheading: 'Rapid prototyping JS framework for modern SPA applications!',
      bodyheading: 'Welcome To The Power of Vue.js!'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
@import '../breakpoints'

.hero
  background: url('../assets/hero.jpg')
  background-size: cover
  min-height: 100vh
  .title
    +mobile
      font-weight: bold
    +tablet
      font-size: 2.5rem
    +desktop
      font-size: 4rem
      margin-top: 2rem

h1, h2, p
  color: #fff

h2
  margin: 1.5rem 0

.section
  background-color: #383838
  .body-heading
    +tablet
      font-size: 2.5rem
    +desktop
      font-size: 2.5rem

</style>
