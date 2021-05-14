<template>
  <div class="home">
    <header-com/>
    <div class="nav">
      <ul class="center">
        <li class="active">首页</li>
        <li>9.9包邮</li>
        <li>超值大额卷</li>
        <li>夏季女装上新</li>
      </ul>
    </div>
    <!-- 菜单 + 轮播图 -->
    <div class="menu-content">
      <Menu/>
      <div class="right">
        <div class="swiper-content">
          <!-- 轮播图 -->
          <div class="swiper">
            <swiper/>
          </div>
          <!-- 轮播图右边 -->
          <div class="swiper-right">
            <h3>9块9包邮</h3>
            <div class="title">保你不吃亏</div>
            <img src="../assets/images/active.gif"
                 alt="ac">
          </div>
        </div>
        <active/>
      </div>
    </div>
    <div class="sub-title">
      <h3>小编精选</h3>
      <p class="title-bar-prompt">每天更新</p>
    </div>
  </div>
</template>

<script>
import Menu from '@/components/menu/index.vue'
import headerCom from '@/components/header/index.vue'
import active from '@/components/active/index.vue'
import swiper from '@/components/swiper/index.vue'

export default {
  name: 'Home',
  components: {
    Menu,
    headerCom,
    active,
    swiper
  },
}
</script>

<style lang="scss" scoped>
.home {
  width: 100%;
  height: 100%;

  .nav {
    width: 100%;
    height: 46px;
    color: #fff;
    background-color: #43240c;
    margin-top: 20px;
    cursor: pointer;

    .center {
      width: 1200px;
      height: 100%;
      margin: 0 auto;
      display: flex;

      li {
        width: 220px;
        height: 100%;
        line-height: 46px;
        list-style: none;
        text-align: center;

        &:hover {
          color: #43240c;
          background-color: #fee44e;
        }
      }

      .active {
        color: #43240c;
        background-color: #fee44e;
      }
    }
  }

  .menu-content {
    width: 1200px;
    height: 370px;
    margin: 0 auto;
    background: #f5f5f5;

    .right {
      width: 980px;
      height: 370px;
      margin-left: 220px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;

      .swiper-content {
        width: 100%;
        height: 234px;
        display: flex;
        justify-content: space-between;

        .swiper {
          width: 660px;
          height: 100%;
        }

        .swiper-right {
          width: 298px;
          height: 234px;
          cursor: pointer;
          box-sizing: border-box;
          float: left;
          position: relative;
          margin-left: 10px;
          padding: 32px 13px;
          background-color: #fff4e4;

          h3 {
            color: #ff5817;
            z-index: 3;
            position: absolute;
            top: 32px;
            left: 13px;
            font-size: 24px;
          }

          .title {
            z-index: 3;
            position: absolute;
            top: 76px;
            left: 0;
            padding: 0 47px 0 22px;
            font-size: 18px;
            line-height: 36px;
            color: #fff;
            background: url('../assets/images/bck.png') no-repeat 50% / cover;
          }

          img {
            z-index: 2;
            position: absolute;
            bottom: 0;
            right: 20px;
            height: 134px;
          }
        }
      }
    }
  }

  .sub-title {
    width: 1200px;
    height: 57px;
    margin: 10px auto 20px;
    font-size: 18px;
    line-height: 56px;
    color: #43240c;
    background-color: #fff;

    h3 {
      display: inline-block;
      margin-left: 52px;
      font-size: 18px;
      font-weight: 500;
    }

    .title-bar-prompt {
      display: inline-block;
      margin-left: 30px;
      font-size: 14px;
      color: #877a73;
    }
  }
}
</style>
