<template lang="">

  <div class="detail-page">
    <div class='video'>
      <video src="http://v3.mukewang.com/shizhan/59f8498ae420e5be578b459b/H.mp4" controls="controls"></video>
      <router-link to="/">
        <div class="video-back"><</div>
      </router-link>
    </div>

    <ul class="nav">
      <li v-for="item in arr">{{ item }}</li>
    </ul>

    <div class="title">
      <h1>{{ title }}</h1>
      <p>{{ des }}</p>
    </div>

    <ul class="question">
      <li v-for="(item,index) in arrQuestion">
        <h1>{{ arrTile[index] }}></h1>
        <p v-html="item"></p>
      </li>
    </ul>
    
  </div>

</template>

<script>
export default {
  data() {
    return {
      arr: [],
      title: "",
      des: "",
      arrQuestion: [],
      arrTile: ["课程须知", "老师告诉你能学到什么？"]
    };
  },
  mounted() {
    this.arr = ["黄忠", "鬼谷子", "妲己", "亚瑟", "明世隐"];

    this.title = "iOS基础教程之-Camera摄像头";
    this.des ="从实例出发介绍我们的Camera，可以实现Camera属性检测，照片拍摄，视频录制，图片展示，录制视频";
    this.arrQuestion = ["本课程适合客户端产品经理，研发人员以及对iOS新特性感兴趣的人群", 
      `
			(1)数码相机相关的所有API<br/> 
			(2)利用Camera实现相机的各种属性检测<br/> 
			(3)利用Camera拍照、保存、遍历相册等功能<br/>
			(4)利用Camera拍摄视频、视频剪切功能`];
  }
};
</script>

<style lang="less" scoped>
.video {
  position: relative;
  height: 191px;
  video {
    width: 100%;
    height: 100%;
  }
  .video-back {
    position: absolute;
    top: 21px;
    left: 16px;
    text-align: center;
    color: #fff;
    font-size: 18px;
    line-height: 32px;
    border-radius: 3px;
    width: 32px;
    height: 32px;
    background: rgba(0, 0, 0, 0.5);
  }
}

.nav {
  position: relative;
  z-index: 1;
  display: flex;
  box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.1);
  li {
    flex: 1;
    display: flex;
    justify-content: center;
    line-height: 44px;
    background: #fff;
    font-size: 14px;
  }
}

.title {
  padding: 24px 0 0 20px;
  h1 {
    font-size: 16px;
    color: #2b333b;
  }
  p {
    font-size: 14px;
    color: #71777d;
    padding: 16px 0 34px;
    width: 335px;
  }
}

.question {
  padding: 20px;
  background: #fff;
  li {
    h1{
      font-size: 14px;
      color: #2b333b;
    }
    p {
      padding: 12px 0 0 30px;
      font-size: 14px;
      color: #71777d;
    }
  }
  li:nth-child(1) {
    padding-bottom: 24px;
  }
}
</style>