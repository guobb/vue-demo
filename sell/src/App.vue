<template>
  <div id="app">
    <v-header></v-header>
    <div class="tap border-1px">
      <div class="tab-item">
        <router-link to="/goods">商品</router-link>
      </div>
      <div class="tab-item">
        <router-link to="/ratings">评论</router-link>
      </div>
      <div class="tab-item">
        <router-link to="/seller">商家</router-link>
      </div>
    </div>
    <router-view></router-view>
  </div>
</template>

<script>
  import header from './components/header/header.vue';

  export default {
      components: {
        'v-header': header
      }
  };
</script>

<style lang="stylus" rel="stylesheet/stylus">
  @import "./common/stylus/mixin.styl";
  .tap
    display: flex
    width: 100%
    height: 40px;
    line-height:40px;
   // border-bottom: 1px solid rgba(1,17,27,0.1)
    border-1px(rgba(1,17,27,0.1))
    .tab-item
      flex:1
      text-align: center
      & > a
        display: block
        font-size: 14px
        color: rgb(77, 85, 93)
      & > a.active {
          color: #f01414;
        }
</style>
