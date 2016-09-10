<template>
  <!-- <div class="nav">
    <ul>
      <li><a v-link="{path:'/newsContent/importNews'}">要闻</a></li>
      <li><a v-link="{path:'/newsContent/business'}">财经</a></li>
      <li><a href="#">体育</a></li>
      <li><a href="#">科技</a></li>
      <li><a href="#">娱乐</a></li>
    </ul>
  </div> -->
  <tab :line-width="1" active-color="#ffd83f" default-color="#57435e">
    <tab-item :selected="demo2 === item.listname" v-for="item in list2" v-link="{path:'/main/mostNew/'+item.trunlink}">
      {{item.listname}}
    </tab-item>
  </tab>
  <router-view></router-view>
</template>

<script>
import {Tab,TabItem} from 'vux';
import 'vux/dist/vux.css';

export default {
  data () {
    return {
      demo2: '推荐',
      list2: [{
        listname:'推荐',
        trunlink:'recommend'
      },{
          listname:'暴漫',
          trunlink:'cartoon'
      },{
          listname:'趣图',
          trunlink:'recommend'
      },{
          listname:'视频',
          trunlink:'recommend'
      },{
          listname:'文字',
          trunlink:'recommend'
      }]
    }
  },
  components:{
    Tab,
    TabItem
  }
};
</script>

<style lang="scss" scoped>

</style>
