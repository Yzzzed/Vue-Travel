<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img :src="item.imgUrl" class="item-img">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1505/c2/0be94f64d9df91.jpg_r_640x214_130f7614.jpg',
        title: '长春世纪影城',
        desc: '长春世纪影城啦啦啦'
      }, {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1505/c2/0be94f64d9df91.jpg_r_640x214_130f7614.jpg',
        title: '长春世纪影城',
        desc: '长春世纪影城啦啦啦'
      }, {
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1505/c2/0be94f64d9df91.jpg_r_640x214_130f7614.jpg',
        title: '长春世纪影城',
        desc: '长春世纪影城啦啦啦'
      }, {
        id: '0004',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1505/c2/0be94f64d9df91.jpg_r_640x214_130f7614.jpg',
        title: '长春世纪影城',
        desc: '长春世纪影城啦啦啦'
      }, {
        id: '0005',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1505/c2/0be94f64d9df91.jpg_r_640x214_130f7614.jpg',
        title: '长春世纪影城',
        desc: '长春世纪影城啦啦啦'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top .2rem
    line-height .8rem
    background #eee
    text-align .2rem
  .item-img-wrapper
    height 0
    overflow hidden
    padding-bottom 33.9%
    .item-img
      width 100%
  .item-info
    padding .1rem
    .item-title
      line-height .54rem
      font-size .32rem
      ellipsis ()
    .item-desc
      line-height .4rem
      color #ccc
      ellipsis ()
</style>
