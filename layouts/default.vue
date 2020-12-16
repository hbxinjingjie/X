<template>
  <div>
    <div class="quanju_left">
      <p style=" border-bottom: 1px solid #fff; margin-top: 15px;">公司全称</p>
      <p>111-1111-1111</p>
    </div>

    <div class="quanju_right_yi">
      联系电话
      <p>11111111111</p>
    </div>
    <div class="quanju_right_er">
      公司地址
      <p>11111111111111111111111111111</p>
    </div>
    <div class="quanju_right_san" @click="fhdb()">返回顶部</div>

    <div class="quanju_yi">
      <img src="" alt="" />

      <div class="quanju_daohang">
        <router-link to="/">首页</router-link>
        <router-link to="/guanyu">关于我们</router-link>
        <router-link to="/qyfc">企业风采</router-link>
        <router-link to="/cxrz">诚信认证</router-link>
        <router-link to="/cpzx">产品中心</router-link>
        <router-link to="/cgal">成功案例</router-link>
        <router-link to="/xwzx">新闻中心</router-link>
        <router-link to="/lxwm">联系我们</router-link>
        <router-link style="color: #5797d5;" to="">进入官网</router-link>
      </div>
    </div>
    <div>
      <img
        src=""
        alt=""
        style="width: 100%; height: 750px; background: #328fcf;"
      />
    </div>
    <Nuxt />
    <div class="quanju_er">
      <div class="quanju_er_a">
        <ul>
          <li class="quanju_b">产品中心</li>
          <li>xxxxxx</li>
          <li>xxxxxx</li>
          <li>xxxxxx</li>
          <li>xxxxxx</li>
          <li>xxxxxx</li>
        </ul>
        <ul>
          <li class="quanju_b">关于我们</li>
          <li>xxxxxx</li>
          <li>xxxxxx</li>
          <li>xxxxxx</li>
          <li>xxxxxx</li>
          <li>xxxxxx</li>
        </ul>
        <ul>
          <li class="quanju_b">成功案例</li>
          <li>xxxxx</li>
          <li>xxxxx</li>
          <li>xxxxx</li>
          <li>xxxxx</li>
          <li>xxxxx</li>
        </ul>
        <ul>
          <li class="quanju_b">联系我们</li>
          <li>xxxxx</li>
          <li><img src="" alt="" style="width: 80px;height: 80px;" /></li>
          <li>技术支持</li>
          <li><img src="" alt="" style="width: 80px;height: 80px;" /></li>
        </ul>
      </div>
      <div class="quanju_er_b"></div>
      <div class="quanju_er_c">
        <span>联系电话</span>
        <p class="p_yi">11111111111</p>
        <span>公司地址</span>
        <p class="p_er">111111111111111111111111111111111111111111111111</p>
      </div>
    </div>
    <div class="quanju_san">
      <p>
        1.
        本页面信息为用户自行上传，本网不对该页面内容（包括但不限于文字、图片、视频）真实性和知识产权负责，如您认为该页面内容侵犯您的权益，请联系我们删除。
      </p>
      <p>
        2.
        本网部分内容转载自其他媒体，目的在于传递更多信息，并不代表本网赞同其观点或证实其内容的真是性。不承担此类作品侵权行为的直接责任及连带责任。
      </p>
      <span>logo公司全称</span>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {};
  },
  methods: {
    fhdb(){
      document.documentElement.scrollTop = document.body.scrollTop = 0;
    }
  }
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
.quanju_yi {
  width: 100%;
  padding: 40px 0;
  background: #1b1b1b;
  display: flex;
  justify-content: space-around;
}
.quanju_yi img {
  width: 100px;
  height: 35px;
  background: #fff;
}
.quanju_yi .quanju_daohang {
  display: inline-block;
}
.quanju_yi .quanju_daohang a {
  text-decoration: none;
  color: #fff;
  padding: 0 20px;
  font-size: 20 px;
}
.quanju_er {
  width: 70%;
  height: 500px;
  padding: 0 15%;
  margin: 0 auto 0;
  background: #0f2b3e;
  display: flex;
}
.quanju_er .quanju_er_a {
  width: 60%;
  padding-top: 100px;
  display: flex;
  color: #fff;
}
.quanju_er .quanju_er_a ul {
  width: 30%;
  list-style: none;
}
.quanju_er .quanju_er_a ul .quanju_b {
  font-size: 22px;
  margin-bottom: 35px;
}
.quanju_er .quanju_er_a li {
  font-size: 19px;
  margin-top: 5px;
}
.quanju_er .quanju_er_b {
  width: 1px;
  height: 300px;
  background: #fff;
  margin-top: 100px;
}
.quanju_er .quanju_er_c {
  width: 300px;
  height: 230px;
  background: #1b1b1b;
  margin: 100px 0 0 100px;
  padding: 50px;
}
.quanju_er .quanju_er_c span {
  color: #fff;
  font-size: 22px;
}
.quanju_er .quanju_er_c p {
  color: #fff;

  font-size: 16px;
  padding-left: 35px;
  margin: 20px 0;
  background-size: 32px;
  background-repeat: no-repeat;
}
.quanju_er .quanju_er_c .p_yi {
  background-image: url(../static/images/quanju_dh.png);
  line-height: 35px;

  color: #328fcf;
}
.quanju_er .quanju_er_c .p_er {
  width: 90%;
  background-image: url(../static/images/quanju_wz.png);
  word-break: break-all;
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 3;
  overflow: hidden;
}
.quanju_san {
  width: 70%;
  height: 140px;
  padding: 0 15%;
  margin: 0 auto;
  background: #000;
  color: #fff;
  padding-top: 10px;
}
.quanju_san p {
  font-size: 14px;
  padding-top: 20px;
}
.quanju_san span {
  display: block;
  float: right;
  margin-top: 15px;
}

.quanju_left {
  width: 190px;
  height: 120px;
  background: #328fcf;
  border-radius: 8px;
  position: absolute;
  top: 300px;
  left: 20px;
  position: fixed;
}
.quanju_left p {
  width: 161px;
  height: 50px;
  line-height: 50px;
  margin: 0 auto;
  text-align: center;
  color: #fff;
}
.quanju_right_yi,
.quanju_right_er,
.quanju_right_san {
  width: 25px;
  height: 100px;
  position: absolute;
  right: 10px;
  position: fixed;
  background: #328fcf;
  color: #fff;
  border-radius: 50px;
  text-align: center;
  padding-top: 10px;
}

.quanju_right_yi {
  top: 180px;
}

.quanju_right_yi p {
  display: none;
}
.quanju_right_yi:hover {
  width: 180px;
  border-radius: 8px;
}
.quanju_right_yi:hover p {
  display: block;
  line-height: 70px;
}

.quanju_right_er {
  top: 320px;
}

.quanju_right_er p {
  display: none;
}
.quanju_right_er:hover {
  width: 140px;
  border-radius: 8px;
  padding-left: 10px;
  padding-right: 10px;
}
.quanju_right_er:hover p {
  display: block;
  word-break: break-all;
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 2;
  overflow: hidden;
  padding-top: 20px;
}

.quanju_right_san {
  top: 450px;
}
</style>
