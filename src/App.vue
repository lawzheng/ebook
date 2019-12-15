<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
  import { mapGetters } from 'vuex'

  export default {
    computed: {
      ...mapGetters(['test'])
    },
    mounted () {
    }
  }
</script>

<style>
</style>
