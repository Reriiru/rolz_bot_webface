<template>
  <div v-bar="{
      preventParentScroll: true,
      scrollThrottle: 30,
  }">
    <div id="app">
      <router-view/>
    </div>
  </div>
</template>

<script>

export default {
  name: 'app'
}
</script>

<style>
</style>
