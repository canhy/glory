<template>
  <div>
  <router-view></router-view>
    <x-header :left-options="{showBack: false}" :right-options='{showMore:true}'>兴欣战队</x-header>
    <div class="vux-demo">
      <img class="logo" src="../assets/images/xingxin.png">
      <h1></h1>
    </div>
    <group>
      <cell v-for='(player,key) in players' :border-intent="false" :title="player.name" is-link :link="player.rout">
        <img slot="icon" width="20" style="display:block;margin-right:5px;" :src="player.portrait">
      </cell>
    </group>
  </div>
</template>

<script>
import { XHeader, Cell, Group, XInput, XButton, CellBox, CellFormPreview } from 'vux'
import yexiu from '../assets/images/yexiu.jpg'
import sumucheng from '../assets/images/sumucheng.jpg'

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
          name: '叶修',
          portrait: yexiu,
          rout: '/xingxin/yexiu',
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
          name: '苏沐橙',
          portrait: sumucheng,
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
