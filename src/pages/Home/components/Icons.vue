<template>

  <swiper :options="swiperOption">
    <swiper-slide>
      <div class='wrapper-icon'>
      <div class='icon' v-for='(item, index) of iconList1' :key='index'>
        <div class='icon-img' :style='{backgroundImage:backgroundObj(item.img)}'></div>
        <div class='icon-desc'>{{item.desc}}</div>
      </div>
    </div>
    </swiper-slide>
    <swiper-slide>
    <div class='wrapper-icon'>
      <div class='icon' v-for='(item, index) of iconList2' :key='index'>
        <div class='icon-img' :style='{backgroundImage:backgroundObj(item.img)}'></div>
        <div class='icon-desc'>{{item.desc}}</div>
      </div>
    </div>
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
</template>

<script>
export default {
  name: 'HomeIcons',

  data () {
    return {
      swiperOption: {
      },
      iconList1: [
        {
          img: '/static/images/icon1.png',
          desc: '飞行'
        },
        {
          img: '/static/images/icon2.png',
          desc: '住房'
        },
        {
          img: '/static/images/icon3.png',
          desc: '古迹'
        },
        {
          img: '/static/images/icon4.png',
          desc: '火车'
        },
        {
          img: '/static/images/icon1.png',
          desc: '飞行'
        },
        {
          img: '/static/images/icon2.png',
          desc: '住房'
        },
        {
          img: '/static/images/icon3.png',
          desc: '古迹'
        },
        {
          img: '/static/images/icon4.png',
          desc: '火车'
        }
      ],
      iconList2: [
        {
          img: '/static/images/icon2.png',
          desc: '住房'
        },
        {
          img: '/static/images/icon1.png',
          desc: '飞行'
        },
        {
          img: '/static/images/icon4.png',
          desc: '火车'
        },
        {
          img: '/static/images/icon3.png',
          desc: '古迹'
        },
        {
          img: '/static/images/icon2.png',
          desc: '住房'
        },
        {
          img: '/static/images/icon1.png',
          desc: '飞行'
        },
        {
          img: '/static/images/icon4.png',
          desc: '火车'
        },
        {
          img: '/static/images/icon3.png',
          desc: '古迹'
        }
      ]
    }
  },

  methods: {
    backgroundObj: function (url) {
      return `url(${url})`
    }
  }
}
</script>

<style lang='stylus' scoped>
.wrapper-icon {
  width: 100%;
  height: 50vw;
  display: flex;
  flex-wrap: wrap;
}

.icon {
  width: 25%;
  height: 50%;

  .icon-img {
    width: 60%;
    height: 60%;
    margin: 0.2rem auto;
    background-size: cover;
    background-position: center;
  }

  .icon-desc {
    color: #333;
    text-align: center;
  }
}
</style>
