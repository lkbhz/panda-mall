<template>
  <div class="header">
    <div class="logo">
      <img class="img"
           src="../../assets/images/logo.png"
           alt="logo">
      <div class="right">
        <h3>熊猫优选</h3>
        <span>XIONG MAO YOU XUAN</span>
      </div>
    </div>
    <div class="input">
      <div class="search">
        <a-input placeholder="搜索更多商品，发现更多优惠"
                 style="width: 330px; margin-left: 50px; border: none"/>
        <a-button type="primary"
                  class="search-button"
                  shape="round">搜索
        </a-button>
      </div>
    </div>
    <div class="advantage">
      <div class="item">
        <img src="../../assets/images/baoyou.png"
             alt="包邮">
        <span>全程包邮</span>
      </div>
      <div class="item">
        <img src="../../assets/images/tuihuan.png"
             alt="tuihuan">
        <span>7天退还</span>
      </div>
      <div class="item">
        <img src="../../assets/images/baoz.png"
             alt="baoz">
        <span>品质保证</span>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'header-com',
}
</script>

<style lang="scss" scoped>
.header {
  width: 1200px;
  height: 100%;
  display: flex;
  margin: 0 auto;

  .logo {
    width: 225px;
    height: 75px;
    margin-top: 50px;
    display: flex;
    justify-content: space-between;
    align-items: center;

    .img {
      width: 75px;
      height: 75px;
    }

    .right {
      text-align: center;

      h3 {
        font-size: 28px;
        font-weight: 600;
        line-height: 40px;
        color: #43200c;
        margin: 0;
      }

      span {
        display: inline-block;
        font-size: 12px;
        line-height: 17px;
        transform: scale(0.8);
      }
    }
  }

  .input {
    height: 48px;
    margin-top: 50px;
    flex: 1;
    display: flex;
    justify-content: center;

    .search {
      width: 532px;
      height: 48px;
      border-radius: 34px;
      box-shadow: inset 0 0 0 2px #43240c;
      background: url('../../assets/images/search.png') no-repeat center left 15px/20px 20px;
      line-height: 48px;

      .search-button {
        width: 120px;
        height: 40px;
        color: #43200c;
        background: #fee44e;
        float: right;
        margin: 4px;
        border: 1px solid #fee44e;
      }
    }
  }

  .advantage {
    width: 182px;
    height: 60px;
    margin-top: 50px;
    display: flex;
    justify-content: space-between;

    .item {
      width: 48px;
      height: 100%;
      font-size: 12px;
      color: #877a73;
      display: flex;
      flex-direction: column;
      justify-content: space-between;

      img {
        width: 40px;
        height: 40px;
      }
    }
  }
}
</style>