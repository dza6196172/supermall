<template>
  <div id="app">
    <router-view></router-view>
    <main-tab-bar/>
  </div>
</template>

<script>
import TabBar from './components/tabbar/TabBar'
import TabBarItem from './components/tabbar/TabBarItem'

export default {
  name:'app',
  components:{
    TabBar,
    TabBarItem
  }
}
</script>

<style>
@import url(./assets/css/base.css);

#tab-bar{
  display: flex;
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
}
.tab-bar-item{
  flex: 1;
  text-align: center;
  background-color: #f5f4f6;
  height: 49px;
  font-size: 14px;
  padding-top: 3px;
}
.tab-bar-item img{
    width: 24px;
    vertical-align: middle;
}
.active{
  color: #d81e06;
}
</style>