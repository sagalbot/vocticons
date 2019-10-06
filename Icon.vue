<template>
  <span v-html="icon"></span>
</template>

<script>
  import icons from 'octicons'

  export default {
    props: ['name'],
    computed: {
      icon () {
        return icons.hasOwnProperty(this.name) ? icons[this.name].toSVG() : ''
      }
    }
  }
</script>

<style type="text/scss" scoped>
  span {
    display: inline-flex;
    align-items: center;
    justify-content: center;
  }
</style>
