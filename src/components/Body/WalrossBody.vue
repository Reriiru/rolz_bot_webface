<template>
    <div class="body-wrapper">
        <el-main>
            <el-container class="bot-image-container around-center column padded_strong">
                <avatar image="https://i.imgur.com/kR5XmXF.png" size="400"> </avatar>
                <el-container class="image-title padded_strong"> Walross Rolz -- a simple bot for PnP games.</el-container>
            </el-container>
            <el-container class="bot-description around-center column padded_strong">
                <el-container class="description-title padded_strong"> Bot summary. </el-container>
                <el-container class="description-text">
                    This bot has some novelty functional, but mostly it is designed for rolling dice
                    and keeping status of your characters. Macros support, as well as index search
                    over your notes in *.md is soon to be added.

                    It uses a rolz.org API and has all of its syntax. It also has some additional functions
                    that API doesn't support. Over all it's pretty noice.
                </el-container>
            </el-container>
            <el-container class="bot-commands column around-center">
                <el-container class="description-title padded_strong">
                    Short reference doc looks something like this:
                </el-container>
                  <b-table
                    :data="isEmpty ? [] : tableDataSimple"
                    :bordered="isBordered">
                    <template slot-scope="props">
                      <b-table-column label="Command" width="40" numeric>
                        {{ props.row.command }}
                      </b-table-column>

                      <b-table-column label="Action">
                        {{ props.row.action }}
                      </b-table-column>
                    </template>
                  </b-table>
                </el-container>
            </el-container>
            <el-container class="bot-demo column around-center">
                <el-container class="description-title padded_strong">
                Here is an embeded bot demo you can play with!
                </el-container>
                <el-container>
                    <embed height='400' width='400' src='https://widgetbot.io/embed/382179952922984449/382179952922984451/0012/' />
                </el-container>
            </el-container>
        </el-main>
    </div>
</template>

<script>
import Avatar from 'vue-avatar-component'

export default {
  name: 'walross-body',
  components: {
    Avatar
  },
  data () {
    const tableDataSimple = [
      {
        command: 'choose',
        action: 'Picks between your variants.'
      }, {
        command: 'nwod or n',
        action: 'Specific format for success based dice for cofd and nwod.'
      }, {
        command: 'roll or r',
        action: 'Gives you a roll, according to Rolz.org syntax'
      }, {
        command: 'repeat',
        action: 'Syntax is !repeat X `roll_query`, rolls multiple time.'
      }, {
        command: 'sum',
        action: 'Syntax is !sum X `roll_query`, rolls multiple time.'
      }, {
        command: 'tarot',
        action: 'Posts a randomized tarot card.'
      }, {
        command: 'value',
        actions: 'This stores your value up to 1000 symbols. The value is unique to your user. Please delete all values after use with demo.'
      }
    ]
    return {
      tableDataSimple,
      isHoverable: true,
      isBordered: true
    }
  }
}
</script>

<style <style lang="scss">
@import "../../colors.scss";

.bot-image-container {
    background-color: $background-light;
}

.image-title {
    font-size: 26px;
    font-weight: bold;
}

.bot-description {
    background-color: $color-secondary;
}

.description-title {
    font-size: 20px;
    justify-content: center;
    width: 100%;
}

.description-text {
    width: 50%;
    text-align: left;
}

.description-reverse {
    width: 50%;
    text-align: left;
    background-color: $background-secondary;
    color: $color-secondary;
}

.bot-commands {
    text-align: left;
}

.b-table {
    width: 70%
}

tr {
    background-color: $background-secondary;
    color: $color-secondary;
}

th {
    background-color: $color-primary;
    color: $color-secondary;
}

</style>