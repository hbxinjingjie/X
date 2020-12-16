<template>
  <div style="width: 70%;margin: 0 auto;">
    <div class="sy_yi">
      <div class="sy_yi_a">
        <h2>xx的<span>产品中心</span></h2>
        <div class="sy_yi_a_a">
          <p></p>
          <span>xxxxxxxx</span>
          <p></p>
        </div>
      </div>
      <div class="sy_yi_b">
        <div class="sy_yi_b_a" v-for="(item,index) in sy_sp" :key="index">
          <img :src="item.img" alt="" />
          <p>{{ item.tit }}</p>
        </div>
      </div>
    </div>
    <div class="sy_er">
      <div class="sy_er_a">
        <h2>xx的<span>关于我们</span></h2>
        <div class="sy_er_a_a">
          <p></p>
          <span>xxxxxxxx</span>
          <p></p>
        </div>
      </div>
      <div class="sy_er_b">
        <div class="sy_er_b_a">
          <span class="sy_er_span_yi">ABOUT US</span>
          <span class="sy_er_span_er"></span>
          <span class="sy_er_span_san">关于我们</span>
          <p>xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx</p>
        <router-link to="/guanyu">查看更多</router-link>

        </div>
      </div>
    </div>
    <div class="sy_san">
      <div class="sy_san_a">
        <h2>xx的<span>成功案例</span></h2>
        <div class="sy_san_a_a">
          <p></p>
          <span>xxxxxxxx</span>
          <p></p>
        </div>
      </div>
      <div class="san_b" v-for="(item,index) in sy_al" :key="index">
        <div class="san_b_a">
          <img src="../static/images/sy_al.jpg" alt="" >
          <div class="san_b_a_a">
            <div style="margin-left: 70px; margin-top: 40px; display: flex;">
                <img :src="item.img" alt="">
                <div>
                  <span>{{item.xingming}}</span>
                <span class="span_er">{{item.zhiwei}}</span>
                <p>{{item.tit}}</p>
                </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="sy_si">
      <div class="sy_si_a">
        <h2>xx的<span>新闻资讯</span></h2>
        <div class="sy_si_a_a">
          <p></p>
          <span>xxxxxxxx</span>
          <p></p>
        </div>
      </div>
      <div class="sy_si_b">
        <div class="sy_si_b_a" v-for="(item,index) in sy_xw" :key="index">
          <div class="sy_si_b_a_yi" >
            {{item.id}}
          </div>
          <div class="sy_si_b_a_er" >
            <span>{{item.tit}}</span>
            <p>{{item.neirong}}</p>
          </div>
       
       </div> 
      
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      sy_xw:[
      {
          id:1,
          tit:'标题',
          neirong:'xxxxxxxxxxxxxxxxxxxxxxxxxxxx'
        },
        {
          id:2,
          tit:'标题',
          neirong:'xxxxxxxxxxxxxxxxxxxxxxxxxxxx'
        },
        {
          id:3,
          tit:'标题',
          neirong:'xxxxxxxxxxxxxxxxxxxxxxxxxxxx'
        },
        {
          id:4,
          tit:'标题',
          neirong:'xxxxxxxxxxxxxxxxxxxxxxxxxxxx'
        },
        {
          id:5,
          tit:'标题',
          neirong:'xxxxxxxxxxxxxxxxxxxxxxxxxxxx'
        },
        {
          id:6,
          tit:'标题',
          neirong:'xxxxxxxxxxxxxxxxxxxxxxxxxxxx'
        },
        {
          id:7,
          tit:'标题',
          neirong:'xxxxxxxxxxxxxxxxxxxxxxxxxxxx'
        },
        {
          id:8,
          tit:'标题',
          neirong:'xxxxxxxxxxxxxxxxxxxxxxxxxxxx'
        },
        {
          id:9,
          tit:'标题',
          neirong:'xxxxxxxxxxxxxxxxxxxxxxxxxxxx'
        },
        {
          id:10,
          tit:'标题',
          neirong:'xxxxxxxxxxxxxxxxxxxxxxxxxxxx'
        },
      ],
      sy_al:[
      {
        zhiwei:'职位职位',
        xingming:'姓名',
        tit:'XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX',
        img:require("~/static/images/sy_al.jpg")
      },   {
        zhiwei:'职位职位',
        xingming:'姓名',
        tit:'XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX',
        img:require("~/static/images/sy_al.jpg")
      },
      ],
      sy_sp: [
        {
          img: require("~/static/images/sy_sp.jpg"),
          tit: "1111111111111"
        },
        {
          img: require("~/static/images/sy_sp.jpg"),
          tit: "1111111111111"
        },
        {
          img: require("~/static/images/sy_sp.jpg"),
          tit: "1111111111111"
        },
        {
          img: require("~/static/images/sy_sp.jpg"),
          tit: "1111111111111"
        },
        {
          img: require("~/static/images/sy_sp.jpg"),
          tit: "1111111111111"
        },
        {
          img: require("~/static/images/sy_sp.jpg"),
          tit: "1111111111111"
        },
        {
          img: require("~/static/images/sy_sp.jpg"),
          tit: "1111111111111"
        },
        {
          img: require("~/static/images/sy_sp.jpg"),
          tit: "1111111111111"
        }
      ]
    };
  }
};
</script>

<style>
.sy_yi {
  width: 100%;
  margin-top: 180px;
}
.sy_yi .sy_yi_a {
  width: 50%;

  margin: 0 auto;
}
.sy_yi .sy_yi_a h2 {
  text-align: center;
  color: #545454;
  font-size: 40px;
  font-weight: normal;
}
.sy_yi .sy_yi_a h2 span {
  color: #328fcf;
}
.sy_yi .sy_yi_a .sy_yi_a_a {
  line-height: 50px;
  display: flex;
  justify-content: space-evenly;
  margin-top: 32px;
}
.sy_yi .sy_yi_a .sy_yi_a_a span {
  font-size: 22px;
  color: #777777;
}
.sy_yi .sy_yi_a .sy_yi_a_a p {
  width: 147px;
  height: 2px;
  background: #777777;
  margin-top: 25px;
}
.sy_yi .sy_yi_b {
  width: 100%;
}
.sy_yi .sy_yi_b .sy_yi_b_a {
  display: inline-block;
  width: 21%;
  margin-left: 3%;
  border-radius: 8px;
  margin-top: 100px;
}
.sy_yi .sy_yi_b .sy_yi_b_a img {
  width: 100%;
  border-radius: 8px;
}
.sy_yi .sy_yi_b .sy_yi_b_a p {
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
  display: none;
  text-align: center;
}
.sy_yi .sy_yi_b .sy_yi_b_a:hover p {
  display: block;
}





.sy_er {
  width: 100%;
  margin-top: 180px;
}
.sy_er .sy_er_a {
  width: 50%;

  margin: 0 auto;
}
.sy_er .sy_er_a h2 {
  text-align: center;
  color: #545454;
  font-size: 40px;
  font-weight: normal;
}
.sy_er .sy_er_a h2 span {
  color: #328fcf;
}
.sy_er .sy_er_a .sy_er_a_a {
  line-height: 50px;
  display: flex;
  justify-content: space-evenly;
  margin-top: 32px;
}
.sy_er .sy_er_a .sy_er_a_a span {
  font-size: 22px;
  color: #777777;
}
.sy_er .sy_er_a .sy_er_a_a p {
  width: 147px;
  height: 2px;
  background: #777777;
  margin-top: 25px;
}
.sy_er .sy_er_b{
  width: 100%;
  height: 522px;
  background: #328fcf;
  margin-top: 100px;
  position: relative;
}
.sy_er .sy_er_b .sy_er_b_a{
  width: 408px;
  height: 288px;
  background: #000;
  opacity: 0.3;
  border-radius: 18px;
  position: absolute;
  top:100px;
  right: 100px;

  padding: 72px 0 0 72px;
}
.sy_er .sy_er_b .sy_er_b_a .sy_er_span_yi{
  font-size: 26px;
  display: block;
  opacity: 1;
color: #fff;
}
.sy_er .sy_er_b .sy_er_b_a .sy_er_span_er{
  display: block;
  width: 46px;
  height: 1px;
  background: #fff;
 margin: 17px 0 18px 0;
}
.sy_er .sy_er_b .sy_er_b_a .sy_er_span_san{
  font-size: 26px;
  display: block;
  opacity: 1;
color: #fff;
}
.sy_er .sy_er_b .sy_er_b_a p{
  width: 80%;
  color: #fff;
  word-break:break-all;
  margin-top: 30px;
  display: -webkit-box;
	-webkit-box-orient: vertical;
	-webkit-line-clamp: 3;
	overflow: hidden;
}
.sy_er .sy_er_b .sy_er_b_a a{
  text-decoration: none;
  color: #fff;
  float: right;
  margin-top: 30px;
  margin-right: 8 0px;
}
















.sy_san {
  width: 100%;
  margin-top: 180px;
}
.sy_san .sy_san_a {
  width: 50%;

  margin: 0 auto;
}
.sy_san .sy_san_a h2 {
  text-align: center;
  color: #545454;
  font-size: 40px;
  font-weight: normal;
}
.sy_san .sy_san_a h2 span {
  color: #328fcf;
}
.sy_san .sy_san_a .sy_san_a_a {
  line-height: 50px;
  display: flex;
  justify-content: space-evenly;
  margin-top: 32px;
}
.sy_san .sy_san_a .sy_san_a_a span {
  font-size: 22px;
  color: #777777;
}
.sy_san .sy_san_a .sy_san_a_a p {
  width: 147px;
  height: 2px;
  background: #777777;
  margin-top: 25px;
}
.sy_san .san_b{
  width: 100%;


  display: flex;

}
.sy_san .san_b .san_b_a{
  width:87%;
  margin: 0 auto;

  display: flex;
  margin-top: 100px;
}
.sy_san .san_b .san_b_a img{
 width: 250px;
 height: 250px;
 border-radius: 20px;
}
.sy_san .san_b .san_b_a_a{
  width: 800px;
  height: 200px;
  background-image: url(../static/images/sy_al_a.png) ; 
 background-size: 100% 100%;
  /* box-shadow:0px 0 15px 0px #000000; */


  background-repeat: no-repeat;
  display: inline-block;
  border-radius: 10px;
  margin-top: 25px;
  margin-left: -100px;
}
.sy_san .san_b .san_b_a_a img{
  width: 60px;
  height: 60px;
  border-radius: 50px;
}
.sy_san .san_b .san_b_a_a span{
  display: block;
  margin-left: 30px;
  margin-top: 10px;
  font-size: 22px;
  color: #328fcf;
}
.sy_san .san_b .san_b_a_a .span_er{
  margin-top: 5px;
  font-size: 16px;
}
.sy_san .san_b .san_b_a_a p{
  width: 500px;
  word-break:break-all;
  margin-top: 10px;
  display: -webkit-box;
	-webkit-box-orient: vertical;
	-webkit-line-clamp: 2;
	overflow: hidden;
  color: #545454;
}











.sy_si {
  width: 100%;
  margin-top: 180px;
  margin-bottom: 180px;
}
.sy_si .sy_si_a {
  width: 50%;

  margin: 0 auto;
}
.sy_si .sy_si_a h2 {
  text-align: center;
  color: #545454;
  font-size: 40px;
  font-weight: normal;
}
.sy_si .sy_si_a h2 span {
  color: #328fcf;
}
.sy_si .sy_si_a .sy_si_a_a {
  line-height: 50px;
  display: flex;
  justify-content: space-evenly;
  margin-top: 32px;
}
.sy_si .sy_si_a .sy_si_a_a span {
  font-size: 22px;
  color: #777777;
}
.sy_si .sy_si_a .sy_si_a_a p {
  width: 147px;
  height: 2px;
  background: #777777;
  margin-top: 25px;
}
.sy_si .sy_si_b{

  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}
.sy_si .sy_si_b .sy_si_b_a{
  width: 40%;
  display: flex;
  height: 100px;
  margin-top: 30px;
}
.sy_si .sy_si_b .sy_si_b_a .sy_si_b_a_yi{
  width: 40px;
   height: 40px; 
   background: #328fcf;
   text-align: center;
   line-height: 40px;
   border-radius: 550px;
   font-size: 26px;
   color: #fff;
   margin-top: 40px;
}
.sy_si .sy_si_b .sy_si_b_a .sy_si_b_a_er{
  width: 350px;
  height: 100px;
  background: #328fcf;
  margin-left: 50px;
  border-radius: 8px;
}
.sy_si .sy_si_b .sy_si_b_a .sy_si_b_a_er span{
  font-size: 30px;
  color: #fff;
  display:block;
  padding-top: 20px;
  width: 70%;
  margin: 0 auto;
}
.sy_si .sy_si_b .sy_si_b_a .sy_si_b_a_er p{
  padding-top: 10px;
  font-size: 16px;
  color: #fff;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  width: 70%;
  margin: 0 auto;
}
</style>
