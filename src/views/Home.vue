<template>
  <div class="home">
    <div id="read" class="test">11</div>
  </div>
</template>

<script>
  // import Epub from 'epubjs'

  // global.ePub = Epub
  export default {
    name: 'home',
    components: {},
    mounted () {
      // this.book = new Epub('/2017_Book_InterdisciplinaryPerspectivesO.epub')
      // this.book.renderTo('read', {
      //   width: window.innerWidth,
      //   height: window.innerHeight
      // }).display()
    }
  }
</script>

<style>
  .test {
    font-size: 50px;
  }
</style>
