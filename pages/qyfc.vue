<template>
    <div style="background: #e7e7e7; padding-bottom: 100px;">
      <div class="qy_yi">
        <div style="width: 70%; margin: 0 auto; display: flex;">
          <div class="ay_yi_a">
            企业风采
          </div>
          <div class="ay_yi_b">
            <p>当前位置</p>
            <el-breadcrumb separator=">">
              <el-breadcrumb-item
                style="color: #545454; margin-top: 40px; margin-left: 10px;"
                :to="{ path: '/' }"
                >首页</el-breadcrumb-item
              >
              <el-breadcrumb-item style="color: #545454; margin-top: 40px;"
                ><a href="/">企业风采</a></el-breadcrumb-item
              >
            </el-breadcrumb>
          </div>
          <div class="ay_yi_c">
           
          </div>
        </div>
      </div>
      <div class="qy_er">
          <div class="qy_er_a">
              <h2>xx的<span>企业风采</span></h2>
              <div class="qy_er_a_a">
                <p></p>
                <span>xxxxxxxx</span>
                <p></p>
              </div>
            </div>
          <div class="qy_er_b">
              <p>0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000011111111111111111111111111111111111111111111111111111111111111111111111111111111112222222222222222222222222222222222222222222222222222222222222222222222222222222233333333333333333333333333333333333333333333333333333333333333333333333333333333444444444444444444444444444444444444444444444444444444444444444444444444444444444455555555555555555555555555555555555555555555555555555555555555555555555555555555</p>
  </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
     
      };
    },
    mounted() {
     
    },
    methods: {
    }
  };
  </script>
  
  <style>
  .qy_yi {
    width: 100%;
    background: #fff;
    margin-top: -5px;
  }
  .qy_yi .ay_yi_a {
    padding: 30px 70px;
    background: #328fcf;
    color: #fff;
    font-size: 30px;
  }
  .qy_yi .ay_yi_b {
    display: flex;
    margin-left: 20px;
    color: #545454;
  }
  .qy_yi .ay_yi_b p {
    height: 50px;
    border-left: 3px solid #328fcf;
    padding-left: 20px;
    line-height: 53px;
    margin-top: 20px;
    color: #545454;
  }
  
  
  
  .qy_er {
    width: 70%;
    margin: 0 auto;
    margin-top: 100px;
      padding-top: 50px;
    background: #fff;
    border-radius: 8px;
  }
  .qy_er .qy_er_a {
    width: 50%;
  
    margin: 0 auto;
  }
  .qy_er .qy_er_a h2 {
    text-align: center;
    color: #545454;
    font-size: 40px;
    font-weight: normal;
  }
  .qy_er .qy_er_a h2 span {
    color: #328fcf;
  }
  .qy_er .qy_er_a .qy_er_a_a {
    line-height: 50px;
    display: flex;
    justify-content: space-evenly;
    margin-top: 32px;
  }
  .qy_er .qy_er_a .qy_er_a_a span {
    font-size: 22px;
    color: #777777;
  }
  .qy_er .qy_er_a .qy_er_a_a p {
    width: 147px;
    height: 2px;
    background: #777777;
    margin-top: 25px;
  }
  .qy_er .qy_er_b{
      width: 85%;
      margin: 0 auto;
  }
  .qy_er .qy_er_b p{
      width: 100%;
      text-indent: 2em;
      padding: 50px 0 80px 0;
      word-break: break-all;
    display: -webkit-box;
    -webkit-box-orient: vertical;
    /* -webkit-line-clamp: 3; */
    overflow: hidden;
    line-height: 30px;
  }
  </style>
  