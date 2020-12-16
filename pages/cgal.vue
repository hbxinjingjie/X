<template>
  <div style="background: #e7e7e7; padding-bottom: 100px;">
    <div class="cgal_yi">
      <div style="width: 70%; margin: 0 auto; display: flex;">
        <div class="cgal_yi_a">
          成功案例
        </div>
        <div class="cgal_yi_b">
          <p>当前位置</p>
          <el-breadcrumb separator=">">
            <el-breadcrumb-item
              style="color: #545454; margin-top: 40px; margin-left: 10px;"
              :to="{ path: '/' }"
              >首页</el-breadcrumb-item
            >
            <el-breadcrumb-item style="color: #545454; margin-top: 40px;"
              ><a href="/">成功案例</a></el-breadcrumb-item
            >
          </el-breadcrumb>
        </div>
        <div class="cgal_yi_c"></div>
      </div>
    </div>
    <div class="cgal_er">
      <div class="cgal_er_a">
        <h2>xx的<span>成功案例</span></h2>
        <div class="cgal_er_a_a">
          <p></p>
          <span>xxxxxxxx</span>
          <p></p>
        </div>
      </div>
      <div class="cgal_er_b">
        <div class="cgal_er_b_a" v-for="(movie) of totalData" :key="movie.id" @click="to(movie)">
         <router-link :to="movie.to" style="text-decoration: none;">
            <img :src="movie.img" alt="" />
            <p>{{ movie.tel }}</p>
         </router-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      totalData: [
        {
          id: 1,
          img: require("~/static/images/sy_sp.jpg"),
          tel: "11111111111111111111111111111111111111111111",
          to:'https://www.baidu.com/'
        },
        {
          id: 2,
          img: require("~/static/images/sy_sp.jpg"),
          tel: "1112211111111111111111111111111111111111111111",
          to:'https://www.baidu.com/'
        },
        {
          id: 3,
          img: require("~/static/images/sy_sp.jpg"),
          tel: "13331111111111111111111111111111111111111111111",
          to:'https://www.baidu.com/'
        },
        {
          id: 4,
          img: require("~/static/images/sy_sp.jpg"),
          tel: "44444444444444",
          to:'https://www.baidu.com/'
        },
        {
          id: 5,
          img: require("~/static/images/sy_sp.jpg"),
          tel: "1115551115511111111111111111111111111111111111111",
          to:'https://www.baidu.com/'
        },
        {
          id: 6,
          img: require("~/static/images/sy_sp.jpg"),
          tel: "1666661111111111111111111111111111111111111111111",
          to:'https://www.baidu.com/'
        },
        {
          id: 7,
          img: require("~/static/images/sy_sp.jpg"),
          tel: "1666661111111111111111111111111111111111111111111",
          to:'https://www.baidu.com/'
        },
        {
          id: 8,
          img: require("~/static/images/sy_sp.jpg"),
          tel: "1666661111111111111111111111111111111111111111111",
          to:'https://www.baidu.com/'
        }
      ]
    };
  },

  methods: {

  },
  methods: {}
};
</script>

<style>
.cgal_yi {
  width: 100%;
  background: #fff;
  margin-top: -5px;
}
.cgal_yi .cgal_yi_a {
  padding: 30px 70px;
  background: #328fcf;
  color: #fff;
  font-size: 30px;
}
.cgal_yi .cgal_yi_b {
  display: flex;
  margin-left: 20px;
  color: #545454;
}
.cgal_yi .cgal_yi_b p {
  height: 50px;
  border-left: 3px solid #328fcf;
  padding-left: 20px;
  line-height: 53px;
  margin-top: 20px;
  color: #545454;
}









.cgal_er {
  width: 70%;
  margin: 0 auto;
  margin-top: 100px;
  padding-top: 50px;
  padding-bottom: 50px;
  background: #fff;
  border-radius: 8px;
}
.cgal_er .cgal_er_a {
  width: 50%;

  margin: 0 auto;
}
.cgal_er .cgal_er_a h2 {
  text-align: center;
  color: #545454;
  font-size: 40px;
  font-weight: normal;
}
.cgal_er .cgal_er_a h2 span {
  color: #328fcf;
}
.cgal_er .cgal_er_a .cgal_er_a_a {
  line-height: 50px;
  display: flex;
  justify-content: space-evenly;
  margin-top: 32px;
}
.cgal_er .cgal_er_a .cgal_er_a_a span {
  font-size: 22px;
  color: #777777;
}
.cgal_er .cgal_er_a .cgal_er_a_a p {
  width: 147px;
  height: 2px;
  background: #777777;
  margin-top: 25px;
}
.cgal_er .cgal_er_b {
  width: 100%;
}
.cgal_er .cgal_er_b .cgal_er_b_a {
  display: inline-block;
  width: 21%;
  margin-left: 3%;
  border-radius: 8px;
  margin-top: 80px;
}
.cgal_er .cgal_er_b .cgal_er_b_a img {
  width: 100%;
  border-radius: 8px;
}
.cgal_er .cgal_er_b .cgal_er_b_a p {
  width: 100%;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  background: #000;
  opacity: 0.3;
  line-height: 60px;
  color: #fff;
  border-bottom-left-radius: 8px;
  border-bottom-right-radius: 8px;
  margin-top: -64px;
  text-align: center;
  
}
</style>
