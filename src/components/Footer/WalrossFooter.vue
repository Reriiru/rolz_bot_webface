<template>
    <div class="footer-wrapper">
        <el-footer class="row arround-center">
            <el-container class="column arround-center footer-left">
                Everything presented here is under MIT License. Full terms and conditions:
                    <el-button size="mini" v-on:click="license">
                        License
                    </el-button>
            </el-container>
            <el-container class="column arround-center footer-right">
                You can contact me via ivelmey@gmail.com.
                If you want to report an issue:
                    <el-button v-on:click="issue" type="secondary" size="mini" >
                        Open Issue
                    </el-button>
            </el-container>
        </el-footer>
    </div>
</template>

<script>
export default {
  name: 'walross-footer',
  methods: {
    license: function () {
      window.location = 'https://github.com/Reriiru/rolz_org_to_discord/blob/master/LICENSE'
    },
    issue: function () {
      window.location = 'https://github.com/Reriiru/rolz_org_to_discord/issues/new'
    }
  }
}
</script>

<style <style lang="scss">

@import "../../colors.scss";

.footer-wrapper {
    background-color: $color-secondary;

    font-size: 12px;
    color: $background-dark;
}

.footer-left {
    
}

.el-button--mini {
    padding: 2px 4px;
    height: 60%;
}

</style>