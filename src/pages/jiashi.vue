<template>
  <div>
    <x-header :left-options="{showBack: false}" :right-options='{showMore:true}'>嘉世战队</x-header>
    <div class="vux-demo">
      <img class="logo" src="../assets/images/jiashi.png">
      <h1></h1>
    </div>
    <group>
      <cell v-for='(player,key) in players' :border-intent="false" :title="player.name" is-link>
        <img slot="icon" width="20" style="display:block;margin-right:5px;" src="">
      </cell>
    </group>
  </div>
</template>

<script>
import { XHeader, Cell, Group, XInput, XButton, CellBox, CellFormPreview } from 'vux'

export default {
  components: {
    XHeader,
    Cell,
    Group,
    XInput,
    XButton,
    CellBox,
    CellFormPreview
  },
  data () {
    return {
      players: [
        {
          name: '孙祥',
          show: false,
          list: [
            {
              label: '角色',
              value: '君莫笑'
            }, {
              label: '职业',
              value: '散人'
            }
          ]
        }, {
          name: '刘皓',
          show: false,
          list: [
            {
              label: '角色',
              value: '沐雨橙风'
            }, {
              label: '职业',
              value: '枪炮'
            }
          ]
        }
      ]
    }
  },
  methods: {
    inquire () {
      console.log(this)
      this.$http.get('api/search?name=@西瓜花').then(function (msg) {
        console.log(msg)
        console.log('1')
      }).catch(function (err) {
        console.log(err)
        console.log('2')
      })
    }
  }
}
</script>

<style>
.vux-demo {
  text-align: center;
}
.logo {
  width: 100px;
  height: 100px
}
</style>
