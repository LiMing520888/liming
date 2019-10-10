<template>
  <div class="c-footer">
   <ul class="footer-ul">
     <li>
       <img src="../../assets/home.png" alt="">
       <span>首页.</span>
     </li>
     <li>
       <img src="../../assets/sea.png" alt="">
       <span>视频.</span>
     </li>
     <li>
       <img src="../../assets/download.png" alt="">
       <span>新闻.</span>
     </li>
     <li>
       <img src="../../assets/me.png" alt="">
       <span>个人中心.</span>
     </li>
   </ul>
  </div>
</template>

<style lang="less" scoped>
  .c-footer {
    position: fixed;
    z-index: 3;
    width: 375px;
    background: #fff;
    border-top: 1px solid #F3F5F7;
    bottom: 0;
    ul {
      display: flex;
      li {
        display: flex;
        height: 50px;
        flex: 1;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        font-size: 10px;
        img {
          width: 24px;
        }
      }
    }
  }
  
</style>