<template>
  <div style="background: #e7e7e7; padding-bottom: 100px;">
    <div class="cpId_yi">
      <div style="width: 70%; margin: 0 auto; display: flex;">
        <div class="cpId_yi_a">
          关于我们
        </div>
        <div class="cpId_yi_b">
          <p>当前位置</p>
          <el-breadcrumb separator=">">
            <el-breadcrumb-item
              style="color: #545454; margin-top: 40px; margin-left: 10px;"
              :to="{ path: '/' }"
              >首页</el-breadcrumb-item
            >
            <el-breadcrumb-item
              style="color: #545454; margin-top: 40px; margin-left: 10px;"
              :to="{ path: '/cpzx' }"
              >产品中心</el-breadcrumb-item
            >
            <el-breadcrumb-item style="color: #545454; margin-top: 40px;"
              ><a href="/">产品详情</a></el-breadcrumb-item
            >
          </el-breadcrumb>
        </div>
        <div class="cpId_yi_c"></div>
      </div>
    </div>
    <div class="cpId_er">
      <div class="cpId_er_a">
        <h2>xx的<span>商品详情</span></h2>
        <div class="cpId_er_a_a">
          <p></p>
          <span>xxxxxxxx</span>
          <p></p>
        </div>
      </div>
      <div class="cpId_er_b">
        <h4>{{ info.aaa }}</h4>
        <p>{{ info.neirong }}</p>
        <img :src="info.img" :alt="info.aaa" :class="info.img ? 'img' : 'imgs'">
        <div></div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      info: {},
      movies: [
        {
          id: 1,
          aaa: "商品",
          neirong:
            "111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111",
          img:  require("~/static/images/sy_sp.jpg"),
        },
        {
          id: 2,
          aaa: "商品",
          neirong: "222222222222"
        },
        {
          id: 3,
          aaa: "商品",
          neirong: "33333333333"
        },
        {
          id: 4,
          aaa: "商品",
          neirong: "44444444444"
        },
        {
          id: 5,
          aaa: "商品",
          neirong: "555555555555"
        },
        {
          id: 6,
          aaa: "商品",
          neirong: "666666666666"
        }
      ]
    };
  },
  mounted() {
    var idx = this.$route.params.id;
    this.info = this.movies.find(item => {
      return item.id == idx;
    });  
  }
};
</script>
<style>
.cpId_yi {
  width: 100%;
  background: #fff;
  margin-top: -5px;
}
.cpId_yi .cpId_yi_a {
  padding: 30px 70px;
  background: #328fcf;
  color: #fff;
  font-size: 30px;
}
.cpId_yi .cpId_yi_b {
  display: flex;
  margin-left: 20px;
  color: #545454;
}
.cpId_yi .cpId_yi_b p {
  height: 50px;
  border-left: 3px solid #328fcf;
  padding-left: 20px;
  line-height: 53px;
  margin-top: 20px;
  color: #545454;
}

.cpId_er {
  width: 70%;
  margin: 0 auto;
  margin-top: 100px;
  padding-top: 50px;
  background: #fff;
  border-radius: 8px;
  padding-bottom: 100px;
}
.cpId_er .cpId_er_a {
  width: 50%;

  margin: 0 auto;
}
.cpId_er .cpId_er_a h2 {
  text-align: center;
  color: #545454;
  font-size: 40px;
  font-weight: normal;
}
.cpId_er .cpId_er_a h2 span {
  color: #328fcf;
}
.cpId_er .cpId_er_a .cpId_er_a_a {
  line-height: 50px;
  display: flex;
  justify-content: space-evenly;
  margin-top: 32px;
}
.cpId_er .cpId_er_a .cpId_er_a_a span {
  font-size: 22px;
  color: #777777;
}
.cpId_er .cpId_er_a .cpId_er_a_a p {
  width: 147px;
  height: 2px;
  background: #777777;
  margin-top: 25px;
}
.cpId_er .cpId_er_b {
  width: 85%;
  margin: 0 auto;
}
.cpId_er .cpId_er_b h4 {
  font-size: 26px;
  text-align: center;
  /* font-weight: normal; */
  margin: 20px 0;
}
.cpId_er .cpId_er_b p {
  padding-bottom: 50px;
  text-indent: 2em;
  width: 100%;
  word-break: break-all;
  display: -webkit-box;
  -webkit-box-orient: vertical;
  /* -webkit-line-clamp: 3; */
  overflow: hidden;
  line-height: 30px;
  font-size: 16px;
}
.cpId_er_b img{
  margin-left: 30%;
}
.cpId_er_b .img{
    display: block;
}
.cpId_er_b .imgs{
    display: none;
}
</style>
