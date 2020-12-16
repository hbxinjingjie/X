<template>
    <div style="background: #e7e7e7; padding-bottom: 100px;">
      <div class="xwzx_yi">
        <div style="width: 70%; margin: 0 auto; display: flex;">
          <div class="xwzx_yi_a">
            新闻中心
          </div>
          <div class="xwzx_yi_b">
            <p>当前位置</p>
            <el-breadcrumb separator=">">
              <el-breadcrumb-item
                style="color: #545454; margin-top: 40px; margin-left: 10px;"
                :to="{ path: '/' }"
                >首页</el-breadcrumb-item
              >
              <el-breadcrumb-item style="color: #545454; margin-top: 40px;"
                ><a href="/">新闻中心</a></el-breadcrumb-item
              >
            </el-breadcrumb>
          </div>
          <div class="xwzx_yi_c">
           
          </div>
        </div>
      </div>
      <div class="xwzx_er">
        <div class="xwzx_er">
            <div class="xwzx_er_a">
              <h2>xx的<span>新闻中心</span></h2>
              <div class="xwzx_er_a_a">
                <p></p>
                <span>xxxxxxxx</span>
                <p></p>
              </div>
            </div>
            <div class="xwzx_er_b" v-for="(movie) of tableData" :key="movie.id" @click="to(movie)">
                <p>{{ movie.tel }}</p>
                <span>{{ movie.shijian }}</span>
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
          tel: "11111111111111111111111111111111111111111111",
          shijian:'2020.12.16'
        },
        {
          id: 2,
          tel: "1112211111111111111111111111111111111111111111",
          shijian:'2020.12.16'
        },
        {
          id: 3,
          tel: "13331111111111111111111111111111111111111111111",
          shijian:'2020.12.16'
        },
        {
          id: 4,
          tel: "44444444444444",
          shijian:'2020.12.16'
        },
        {
          id: 5,
          tel: "1115551115511111111111111111111111111111111111111",
          shijian:'2020.12.16'
        },
        {
          id: 6,
          tel: "1666661111111111111111111111111111111111111111111",
          shijian:'2020.12.16'
        },
        {
          id: 7,
          tel: "1666661111111111111111111111111111111111111111111",
          shijian:'2020.12.16'
        },
        {
          id: 8,
          tel: "166666111111111111111111111111111111111111111111116666611111111111111111111111111111111111111111111666661111111111111111111111111111111111111111111",
          shijian:'2020.12.16'
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
      this.$router.push("/xwzx/" + obj.id);
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
  .xwzx_yi {
    width: 100%;
    background: #fff;
    margin-top: -5px;
  }
  .xwzx_yi .xwzx_yi_a {
    padding: 30px 70px;
    background: #328fcf;
    color: #fff;
    font-size: 30px;
  }
  .xwzx_yi .xwzx_yi_b {
    display: flex;
    margin-left: 20px;
    color: #545454;
  }
  .xwzx_yi .xwzx_yi_b p {
    height: 50px;
    border-left: 3px solid #328fcf;
    padding-left: 20px;
    line-height: 53px;
    margin-top: 20px;
    color: #545454;
  }
  
  
  




  .xwzx_er {
  width: 70%;
  margin: 0 auto;
  margin-top: 100px;
  background: #fff;
}
.xwzx_er .xwzx_er_a {
  width: 50%;
padding-top: 100px;
  margin: 0 auto;
}
.xwzx_er .xwzx_er_a h2 {
  text-align: center;
  color: #545454;
  font-size: 40px;
  font-weight: normal;
}
.xwzx_er .xwzx_er_a h2 span {
  color: #328fcf;
}
.xwzx_er .xwzx_er_a .xwzx_er_a_a {
  line-height: 50px;
  display: flex;
  justify-content: space-evenly;
  margin-top: 32px;
}
.xwzx_er .xwzx_er_a .xwzx_er_a_a span {
  font-size: 22px;
  color: #777777;
}
.xwzx_er .xwzx_er_a .xwzx_er_a_a p {
  width: 147px;
  height: 2px;
  background: #777777;
  margin-top: 25px;
}
.xwzx_er .xwzx_er_b {
  width: 100%;
  display: flex;
  justify-content: space-between;
  border-bottom: 1px dashed #333;
  padding: 27px 0;
}
.xwzx_er .xwzx_er_b p {
    width: 60%;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  /* line-height: 60px; */
  padding-left: 20px;
  background-image: url(../../static/images/sanjiao_right.png);
  background-repeat: no-repeat;
  background-size: 20px;
}
.xwzx_er .xwzx_er_b span {
  /* line-height: 60px; */
}

.block{
    text-align: center;
    /* margin: 30px 0 50px 0; */
    padding: 40px 0 60px 0;
}
  </style>
  