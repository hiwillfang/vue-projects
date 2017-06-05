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
  </div>
</template>

<script>
export default {
  name: 'home',
  data() {
    return {
      heading: 'Vue.js Web Application',
      subheading: 'Rapid prototyping JS framework for modern SPA applications!'
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
  min-height: 600px
  .title
    +mobile
      font-weight: bold
    +tablet
      font-size: 2.5rem
    +desktop
      font-size: 4rem
      margin-top: 2rem

h1, h2
  color: #fff

h2
  margin: 1.5rem 0

</style>
