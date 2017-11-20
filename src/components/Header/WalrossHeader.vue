<template>
    <div class="header-wrapper">
        <el-header class="align-center">
            <el-container>
                <el-button v-on:click="toGit" type="primary">
                    <i class="fa fa-github" aria-hidden="true"></i>
                    Project's Github
                </el-button>
                <el-button v-on:click="inviteLink" type="primary">
                    <i class="fa fa-share-alt" aria-hidden="true"></i>
                    Discord invite
                </el-button>
            </el-container>
        </el-header>
    </div>
</template>

<script>
export default {
  name: 'walross-header',
  methods: {
    toGit: function () {
      window.location = 'https://github.com/Reriiru/rolz_org_to_discord/'
    },
    inviteLink: function () {
      window.location = 'https://discordapp.com/oauth2/authorize?client_id=376342947077160960&scope=bot&permissions=84992'
    }
  }
}
</script>

<style <style lang="scss">
@import '../../colors.scss';

.header-wrapper { 
    background-color: $background-dim;
    width: 100%;
}

</style>
