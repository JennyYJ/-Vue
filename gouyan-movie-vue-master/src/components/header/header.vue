<template>
  <div>
    <div class="v-header">
      <div class="v-header-logo">
        <div>
          <img src="../../assets/logo.png">
        </div>
        <div class="v-load-title">
          <h3>iMoive</h3>
          <div>分享与沉浸</div> 
        </div>
      </div>
      <div class="v-header-input" @click="search">
        <router-link to="/searchPage" class="v-nav">个人推荐</router-link>
      </div>
    </div>
    <div class="v-nav-bar">
      <router-link to="/inTheaters" class="v-nav">高分电影</router-link>
      <router-link to="/comingSoon" class="v-nav">即将上映</router-link>
    </div>
    <div>
      
    </div>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        query: ''
      }
    },
    methods: {
      search: function () {
        this.$router.push({path: '/searchPage'})
      }
    }
  }
</script>

<style>
  .v-header {
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    height: 60px;
    padding: 10px 20px;
    box-sizing: border-box;
  }
  .v-header-logo {
    flex: 1;
  }
  .v-header-logo > div {
    display: inline-block;
  }
  .v-header-logo > div:first-child img{
    height: 42px;
    width: 42px;
  }
  .v-header-logo > div:last-child {
    vertical-align: top;
  }
  .v-header-input {
    width: 100px;
    line-height: 100%;
  }
  .v-load-title h3 {
    font-size: 20px;
    font-weight: 700;
    color: rgb(167, 151, 151);
  }
  .v-load-title div {
    font-size: 12px;
    color: #999;
  }
  .v-nav-bar {
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    background-color: #222121;
    border-bottom: 1px solid #d6d6d6;
  }
  .v-nav {
    flex: 1;
    text-align: center;
    text-decoration: none;
    height: 35px;
    line-height: 35px;
    font-size: 20px;
    color: #F9FAFC;
  }
  .v-inp {
    width: 100%;
    height: 40px;
    border-style: none;
    border-radius: 15px;
    padding-left: 10px;
  }
</style>
