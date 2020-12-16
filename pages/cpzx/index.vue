<template>
    <div style="background: #e7e7e7; padding-bottom: 100px;">
      <div class="cpzx_yi">
        <div style="width: 70%; margin: 0 auto; display: flex;">
          <div class="cpzx_yi_a">
            产品中心
          </div>
          <div class="cpzx_yi_b">
            <p>当前位置</p>
            <el-breadcrumb separator=">">
              <el-breadcrumb-item
                style="color: #545454; margin-top: 40px; margin-left: 10px;"
                :to="{ path: '/' }"
                >首页</el-breadcrumb-item
              >
              <el-breadcrumb-item style="color: #545454; margin-top: 40px;"
                ><a href="/">产品中心</a></el-breadcrumb-item
              >
            </el-breadcrumb>
          </div>
          <div class="cpzx_yi_c">
           
          </div>
        </div>
      </div>
      <div class="cpzx_er">
       
            <div class="cpzx_er_a">
              <h2>xx的<span>产品中心</span></h2>
              <div class="cpzx_er_a_a">
                <p></p>
                <span>xxxxxxxx</span>
                <p></p>
              </div>
            </div>
            <div class="cpzx_er_b">
              <div class="cpzx_er_b_a" v-for="(movie) of tableData" :key="movie.id" @click="to(movie)">
                <img :src="movie.img" alt="" />
                <p>{{ movie.tel }}</p>
              </div>
            
          </div>
          <div class="block">
            <el-pagination
              @size-change="handleSizeChange"
              @current-change="handleCurrentChange"
              :current-page="currentPage"
              :page-sizes="[10, 20, 30, 40]"
              :page-size="pagesize"
              layout="total, sizes, prev, pager, next, jumper"
              :total="totalData.length"
            >
            </el-pagination>
          </div>
  </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        pagesize:8, //刷新页面后每一页有3条数据
      currentPage: 1, //刷新页面后当前页为第一页
      totalData: [
        {
          id: 1,
          img:  require("~/static/images/sy_sp.jpg"),
          tel: "11111111111111111111111111111111111111111111",
        },
        {
          id: 2,
          img: require("~/static/images/sy_sp.jpg"),
          tel: "1112211111111111111111111111111111111111111111",
        },
        {
          id: 3,
          img: require("~/static/images/sy_sp.jpg"),
          tel: "13331111111111111111111111111111111111111111111",
        },
        {
          id: 4,
          img: require("~/static/images/sy_sp.jpg"),
          tel: "44444444444444",
        },
        {
          id: 5,
          img:  require("~/static/images/sy_sp.jpg"),
          tel: "1115551115511111111111111111111111111111111111111",
        },
        {
          id: 6,
          img: require("~/static/images/sy_sp.jpg"),
          tel: "1666661111111111111111111111111111111111111111111",
        },
        {
          id: 7,
          img: require("~/static/images/sy_sp.jpg"),
          tel: "1666661111111111111111111111111111111111111111111",
        },
        {
          id: 8,
          img: require("~/static/images/sy_sp.jpg"),
          tel: "1666661111111111111111111111111111111111111111111",
        },
      ],
       
      };
    },
    computed: {
    tableData() {
      return this.totalData.slice(
        this.pagesize * (this.currentPage - 1),
        this.pagesize * this.currentPage
      );
    },
  },
  methods: {
    to(obj) {
      this.$router.push("/cpzx/" + obj.id);
    },
    handleSizeChange(val) {
      console.log(`每页 ${val} 条`);
      this.pagesize = val;
    },
    handleCurrentChange(val) {
      console.log(`当前页: ${val}`);
      // this.currentPage = val;    //动态改变
      this.currentPage = val;
    },
}
  };
  </script>
  
  <style>
  .cpzx_yi {
    width: 100%;
    background: #fff;
    margin-top: -5px;
  }
  .cpzx_yi .cpzx_yi_a {
    padding: 30px 70px;
    background: #328fcf;
    color: #fff;
    font-size: 30px;
  }
  .cpzx_yi .cpzx_yi_b {
    display: flex;
    margin-left: 20px;
    color: #545454;
  }
  .cpzx_yi .cpzx_yi_b p {
    height: 50px;
    border-left: 3px solid #328fcf;
    padding-left: 20px;
    line-height: 53px;
    margin-top: 20px;
    color: #545454;
  }
  
  
  




  .cpzx_er {
  width: 70%;
  margin: 0 auto;
  margin-top: 100px;
  background: #fff;
}
.cpzx_er .cpzx_er_a {
  width: 50%;
padding-top: 100px;
  margin: 0 auto;
}
.cpzx_er .cpzx_er_a h2 {
  text-align: center;
  color: #545454;
  font-size: 40px;
  font-weight: normal;
}
.cpzx_er .cpzx_er_a h2 span {
  color: #328fcf;
}
.cpzx_er .cpzx_er_a .cpzx_er_a_a {
  line-height: 50px;
  display: flex;
  justify-content: space-evenly;
  margin-top: 32px;
}
.cpzx_er .cpzx_er_a .cpzx_er_a_a span {
  font-size: 22px;
  color: #777777;
}
.cpzx_er .cpzx_er_a .cpzx_er_a_a p {
  width: 147px;
  height: 2px;
  background: #777777;
  margin-top: 25px;
}
.cpzx_er .cpzx_er_b {
  width: 100%;
}
.cpzx_er .cpzx_er_b .cpzx_er_b_a {
  display: inline-block;
  width: 21%;
  margin-left: 3%;
  border-radius: 8px;
  margin-top: 80px;
}
.cpzx_er .cpzx_er_b .cpzx_er_b_a img {
  width: 100%;
  border-radius: 8px;
}
.cpzx_er .cpzx_er_b .cpzx_er_b_a p {
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

.block{
    text-align: center;
    /* margin: 30px 0 50px 0; */
    padding: 40px 0 60px 0;
}
  </style>
  