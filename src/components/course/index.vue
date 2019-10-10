<template>
  <ul
    class="c-course"
    tag="a"
  >
    <router-link
      to="/detail"
      class="nihao1"
    >
      <li v-for="item in arrList">
        <img :src="item.imgUrl" />
        <h1>{{item.title}}</h1>
        <p>{{item.msg}}</p>
      </li>
    </router-link>
  </ul>
</template>
<script>
export default {
  props: {
    arrList: Array
  }
};
</script>

<style lang="less" scoped>
.c-course {
  padding: 24px 0;
  background: #fff;
  margin-bottom: 33px;
  a {
    text-decoration: none;
    li {
      position: relative;
      width: 335px;
      height: 72px;
      margin: 0 auto;
      img {
        position: absolute;
        width: 108px;
        border-radius: 5px;
      }
      h1 {
        font-size: 15px;
        padding-left: 124px;
        color: #2b333b;
      }
      p {
        font-size: 12px;
        padding: 8px 0 0 124px;
        color: #71777d;
      }
    }
  }
}
</style>