<template>
  <div class='home_model'>
    <swiper :options="swiperOption" class='sw_model'>
      <swiper-slide v-for='(troop,i) in troops' class='sw_bg'>
        <div class="vux-demo">
          <img class="logo" :src="troop.logo">
        </div>
        <group :title='troop.slogan'>
          <cell v-for='(player,key) in troop.players' :border-intent="false" :title="player.name" is-link>
            <img slot="icon" width="20" style="display:block;margin-right:5px;" src="">
          </cell>
        </group>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
import { XHeader, Cell, Group, XInput, XButton, CellBox, CellFormPreview } from 'vux'
import lanyulogo from '../assets/images/lanyu.png'
import lunhuilogo from '../assets/images/lunhui.png'
import xingxinlogo from '../assets/images/xingxin.png'
import jiashilogo from '../assets/images/jiashi.png'
import weicaologo from '../assets/images/weicao.png'
import batulogo from '../assets/images/batu.png'

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
      swiperOption: {
        mousewheelControl: true,
        effect: 'cube',
        cube: {
          slideShadows: true,
          shadow: true,
          shadowOffset: 100,
          shadowScale: 0.6
        },
        autoHeight: true,
        loop: true
      },
      troops: [{
        logo: lanyulogo,
        slogan: '我们还有很多个属于蓝雨的夏天',
        players: [
          {
            name: '喻文州'
          }, {
            name: '黄少天'
          }, {
            name: '卢瀚文'
          }, {
            name: '郑轩'
          }, {
            name: '宋晓'
          }, {
            name: '李远'
          }, {
            name: '徐景熙'
          }
        ]
      }, {
        logo: lunhuilogo,
        slogan: '我始终相信轮回可以获胜，无论对手是谁',
        players: [
          {
            name: '郑泽楷'
          }, {
            name: '江波涛'
          }, {
            name: '杜明'
          }, {
            name: '方明华'
          }, {
            name: '吕泊远'
          }, {
            name: '吴起'
          }
        ]
      }, {
        logo: xingxinlogo,
        slogan: '兴欣之火,可以燎原',
        players: [
          {
            name: '叶修'
          }, {
            name: '苏沐橙'
          }, {
            name: '方锐'
          }, {
            name: '唐柔'
          }, {
            name: '包荣兴'
          }, {
            name: '乔一帆'
          }, {
            name: '逻辑'
          }, {
            name: '莫凡'
          }, {
            name: '安文逸'
          }, {
            name: '魏琛'
          }
        ]
      }, {
        logo: jiashilogo,
        slogan: '嘉世不会倒',
        players: [
          {
            name: '孙祥'
          }, {
            name: '刘皓'
          }, {
            name: '吴雪峰'
          }, {
            name: '郭阳'
          }, {
            name: '王泽'
          }, {
            name: '张家兴'
          }, {
            name: '申建'
          }, {
            name: '贺铭'
          }, {
            name: '邱非'
          }
        ]
      }, {
        logo: weicaologo,
        slogan: '区区微草，生于毫末，毫末之草，可以成原',
        players: [
          {
            name: '王杰希'
          }, {
            name: '许斌'
          }, {
            name: '刘小别'
          }, {
            name: '高英杰'
          }, {
            name: '袁柏青'
          }, {
            name: '周烨柏'
          }, {
            name: '梁方'
          }, {
            name: '肖云'
          }, {
            name: '柳非'
          }, {
            name: '李济'
          }
        ]
      }, {
        logo: batulogo,
        slogan: '十年霸图，一如既往',
        players: [
          {
            name: '韩文清'
          }, {
            name: '张新杰'
          }, {
            name: '张佳乐'
          }, {
            name: '白言飞'
          }, {
            name: '秦牧云'
          }, {
            name: '宋奇英'
          }, {
            name: '郑乘风'
          }, {
            name: '于天'
          }
        ]
      }, {
        logo: xingxinlogo,
        slogan: '相信自己的团队，那是胜利的信仰',
        players: [
          {
            name: '肖时钦'
          }, {
            name: '方学才'
          }, {
            name: '戴研琦'
          }, {
            name: '程泰'
          }, {
            name: '鲁奕宁'
          }, {
            name: '张家兴'
          }
        ]
      }, {
        logo: xingxinlogo,
        slogan: '虚空可以六年没有最佳组合，但不能一秒没有双鬼',
        players: [
          {
            name: '李轩'
          }, {
            name: '吴羽策'
          }, {
            name: '李迅'
          }, {
            name: '盖才捷'
          }, {
            name: '葛兆蓝'
          }, {
            name: '杨昊轩'
          }, {
            name: '唐礼升'
          }
        ]
      }, {
        logo: xingxinlogo,
        slogan: '双花哪里够？要百花才好',
        players: [
          {
            name: '叶修'
          }, {
            name: '苏沐橙'
          }
        ]
      }, {
        logo: xingxinlogo,
        slogan: '刺客亡命之日，谁都不可独活',
        players: [
          {
            name: '杨聪'
          }, {
            name: '白庶'
          }, {
            name: '高杰'
          }, {
            name: '李亦辉'
          }, {
            name: '钱文举'
          }, {
            name: '孙明进'
          }
        ]
      }, {
        logo: xingxinlogo,
        slogan: '我会用最柔弱的肩膀，撑起那一座烟雨楼',
        players: [
          {
            name: '楚云秀'
          }, {
            name: '李华'
          }, {
            name: '舒可欣'
          }, {
            name: '舒可怡'
          }, {
            name: '孙亮'
          }, {
            name: '冯向明'
          }, {
            name: '白祁'
          }
        ]
      }, {
        logo: xingxinlogo,
        slogan: '以下克上，势不可挡',
        players: [
          {
            name: '唐昊'
          }, {
            name: '赵宇哲'
          }, {
            name: '阮永彬'
          }
        ]
      }]
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
.home_model {
  height: 100%;
}
.sw_model {
  height: 100% !important;
}
.sw_bg {
  background: #fbf9fe;
  height: 100% !important;
}
.vux-demo {
  text-align: center;
}
.logo {
  width: 100px;
  height: 100px
}
</style>
