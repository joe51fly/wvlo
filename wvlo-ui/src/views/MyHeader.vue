<template>
  <div>
      <el-backtop  :bottom="100">
        <div id="backTopDiv">
          Top
        </div>
      </el-backtop>
    <div id="linkDiv">
<!--      <router-link :to="{path:'live-list',param:{list:list}}">直播</router-link>-->
      <div id="userDiv">
        <el-avatar :src="imgUrl"></el-avatar>
        <span v-model="userName"></span>
        <el-dropdown>
          <i class="el-icon-arrow-down"></i>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item>查看</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
      </div>
    </div>
  </div>
</template>


<script>
  import $ from 'jquery';

  export default {
    name: 'myHeader',
    props: {
      list: Array
    },
    data() {
      return {
        imgUrl: "https://cube.elemecdn.com/3/7c/3ea6beec64369c2642b92c6726f1epng.png",
        userName:'王小虎'
      }
    },
    methods: {},
    mounted() {

    },
  }
</script>

<style>
  #userDiv{
    text-align: right;
    display: inline;
    justify-content: flex-end;
    flex: 1px;
  }
  #backTopDiv{
    height: 100%;
    width: 100%;
    background-color: #f2f5f6;
    box-shadow: 0 0 6px rgba(0,0,0, .12);
    text-align: center;
    line-height: 40px;
    color: #1989fa;
  }
  #linkDiv{
    display: flex;
    margin-left: 50px;
  }

  i {
    background-position: center;
    font-size: 20px;
    margin-right: 1rem;
  }

  .el-avatar {
    border: none;
    vertical-align: middle;
    margin-left: 10px;
  }

</style>
