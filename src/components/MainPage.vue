<template>
  <div class="main-wrapper">    
            <walross-header></walross-header>
            <walross-body></walross-body>
            <walross-footer></walross-footer>
  </div>
</template>

<script>
import WalrossHeader from './Header/WalrossHeader'
import WalrossBody from './Body/WalrossBody'
import WalrossFooter from './Footer/WalrossFooter'

export default {
  name: 'main-page',
  components: {
    WalrossHeader,
    WalrossBody,
    WalrossFooter
  },
  data () {
    return {
      msg: 'This is WalrossRolz main page, you are welcome!'
    }
  }
}
</script>

<style <style lang="scss">
.wrapper {
  height: auto;
  width: auto;
}
</style>