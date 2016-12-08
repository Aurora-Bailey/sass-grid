<template>
  <div id="app">
    <img src="./assets/logo.png">
    <hello></hello>
    <div class="qwerty">
      <div class="q">q</div>
      <div class="w">
        <div class="e">e</div>
        <div class="r">r</div>
        <div class="t">t</div>
      </div>
    </div>
  </div>
</template>

<script>
import Hello from './components/Hello'

export default {
  name: 'app',
  components: {
    Hello
  }
}
</script>

<style lang="sass">
  @import "sass/main"

  #app
    font-family: 'Avenir', Helvetica, Arial, sans-serif
    -webkit-font-smoothing: antialiased
    -moz-osx-font-smoothing: grayscale
    text-align: center
    color: #2c3e50
    margin-top: 60px

    width: 1200px
    margin-left: auto
    margin-right: auto
    +mobile(1200px)
      width: 600px
    +mobile(600px)
      width: 400px
    +mobile(400px)
      width: auto

  .qwerty
    +border-radius(50px)
    background-color: darken($primary, 25%)
    +contain()

    .q
      +span(4, 12)
      outline: 1px solid lime

    .w
      +span(8,12)
      +contain()
      outline: 1px solid blue

      .e
        +span(4, 12)
        outline: 1px solid lime
      .r
        +span(4, 12)
        outline: 1px solid lime
      .t
        +span(4, 12)
        outline: 1px solid lime

      +mobile(1200px)
        .e
          +span(4, 8)
          outline: 1px solid lime
        .r
          +span(4, 8)
          outline: 1px solid lime
        .t
          +span(8, 8)
          outline: 1px solid lime

  .asdf
    color: pink
</style>
