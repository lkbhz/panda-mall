<template>
  <div class="home">
    <div class="hearder">
      <div class="logo">
        <img class="img"
             src="../assets/images/logo.png"
             alt="logo">
        <div class="right">
          <h3>熊猫优选</h3>
          <span>XIONG MAO YOU XUAN</span>
        </div>
      </div>
      <div class="input">
        <div class="seach">
          <a-input placeholder="搜索更多商品，发现更多优惠"
                   style="width: 330px; margin-left: 50px; border: none" />
          <a-button type="primary"
                    class="search-button"
                    shape="round">搜索</a-button>
        </div>
      </div>
      <div class="advantage">
        <div class="item">
          <img src="../assets/images/baoyou.png"
               alt="包邮">
          <span>全程包邮</span>
        </div>
        <div class="item">
          <img src="../assets/images/tuihuan.png"
               alt="tuihuan">
          <span>7天退还</span>
        </div>
        <div class="item">
          <img src="../assets/images/baoz.png"
               alt="baoz">
          <span>品质保证</span>
        </div>
      </div>
    </div>
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
      <Menu />
      <div class="right">
        <div class="swiper-content">
          <!-- 轮播图 -->
          <div class="swiper"></div>
          <!-- 轮播图右边 -->
          <div class="swiper-right">
            <h3>9块9包邮</h3>
            <div class="title">保你不吃亏</div>
            <img src="../assets/images/active.gif"
                 alt="ac">
          </div>
        </div>
        <div class="right-bottom">
          <div class="img pink">
            <h3>夏季女装上新</h3>
            <p>速来抢购~</p>
            <span>Go</span>
            <img src="http://img1.lukou.com/static/coupon/p/image_link/vsaRLJUT8OSbh1yM9d0nPQk8vptgNbSQ.png"
                 alt="">
          </div>
          <div class="img yellow">
            <h3>夏季女装上新</h3>
            <p>速来抢购~</p>
            <span>Go</span>
            <img src="http://img1.lukou.com/static/p/commodity/img/20181212-235507.png"
                 alt="">
          </div>
          <div class="img blue">
            <p>扫码下载APP</p>
            <p>发现更多惊喜</p>
            <img class="qrcode"
                 src="../assets/images/code.png"
                 alt="">
          </div>
        </div>
      </div>
    </div>
    <div class="sub-title">
      <h3>小编精选</h3>
      <p class="title-bar-prompt">每天更新</p>
    </div>
    <div class="choice">
      <ul class="base-commodity-list">
        <li class="base-commodity-list-item">
          <div class="commodity-card">
            <div class="commodity-container">
              <img src="../assets/images/pic.jpg"
                   alt="">
            </div>
            <div class="commodity-card-msg">
              <div class="commodity-card-title">
                雅酷美迷你充电宝原装正品大容量20000毫安小巧自带四线超薄便携2
              </div>
              <div class="commodity-card-keyword">
                <span class="keyword tmall">天猫</span>
                <span class="keyword free-postage">包邮</span>
              </div>
              <div class="commodity-card-foot">
                <div class="left">
                  ￥99999
                </div>
                <div class="coupon-value">
                  10元券
                </div>
              </div>
            </div>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
  // @ is an alias to /src
  import Menu from '@/components/menu/index.vue'

  export default {
    name: 'Home',
    components: {
      Menu,
    },
  }
</script>

<style lang="scss" scoped>
  .home {
    // width: 100%;
    // height: 100%;
    .hearder {
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
        .seach {
          width: 532px;
          height: 48px;
          border-radius: 34px;
          box-shadow: inset 0 0 0 2px #43240c;
          background: url('../assets/images/search.png') no-repeat center left 15px/20px 20px;
          line-height: 48px;
          .search-button {
            width: 120px;
            height: 40px;
            margin-left: 10px;
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
    .nav {
      width: 100%;
      height: 46px;
      color: #fff;
      background-color: #43240c;
      margin-top: 20px;
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
            border: 1px solid #000;
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
        .right-bottom {
          width: 100%;
          height: 128px;
          display: flex;
          justify-content: space-between;
          .img {
            width: 320px;
            height: 100%;
            position: relative;
            padding: 26px 34px 16px;
            color: #fff;
            border-radius: 18px;
            h3 {
              font-size: 22px;
              font-weight: 600;
              margin: 0;
            }
            p {
              font-size: 18px;
              margin: 0;
            }
            span {
              display: block;
              margin-top: 11px;
              width: 47px;
              font-size: 14px;
              line-height: 20px;
              text-align: center;
              color: #fec17e;
              background-color: #fff;
              border-radius: 10px;
              color: #fca6c0;
            }
            img {
              position: absolute;
              bottom: 0;
              right: 0;
              width: 125px;
              height: 125px;
            }
          }
          .pink {
            background: linear-gradient(270deg, #ffd1dd, #fca6c0);
          }
          .yellow {
            background: linear-gradient(270deg, #fffffe, #fec07e);
          }
          .blue {
            font-size: 18px;
            color: #fff;
            background: linear-gradient(270deg, #e7f5ff, #afdcff);
            .qrcode {
              box-sizing: border-box;
              position: absolute;
              top: 14px;
              right: 20px;
              width: 100px;
              height: 100px;
              background-color: #fff;
              border-radius: 18px;
              border: 8px solid #afdcff;
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
    .choice {
      width: 1200px;
      margin: 0 auto;
      padding: 0 16px;
      background: #f6f6f6;
      .base-commodity-list {
        overflow: hidden;
        min-height: 40vh;
        .base-commodity-list-item {
          cursor: pointer;
          display: block;
          float: left;
          margin-right: 21px;
          width: 276px;
          height: 389px;
          overflow: hidden;
          margin-bottom: 22px;
          position: relative;
          box-sizing: border-box;
          transition: all 0.3s;
          .commodity-card {
            background-color: #fff;
            display: inline-block;
            width: 100%;
            height: 100%;
            position: relative;
            border: none;
            .commodity-container {
              overflow: hidden;
              position: relative;
              padding-top: 100%;
              width: 100%;
              display: block;
              img {
                position: absolute;
                top: 50%;
                left: 50%;
                height: 100%;
                display: block;
                transform: translate(-50%, -50%);
              }
            }
            .commodity-card-msg {
              padding: 10px 17px 17px;
              box-sizing: border-box;
              .commodity-card-title {
                overflow: hidden;
                font-size: 14px;
                line-height: 18px;
                text-overflow: ellipsis;
                color: #877a73;
                white-space: nowrap;
              }
              .commodity-card-keyword {
                position: relative;
                margin: 16px auto 0;
                .keyword {
                  padding: 0 10px;
                  color: #fff;
                  border-radius: 2px;
                  box-shadow: none;
                }
                .tmall {
                  background-color: #df2b2f;
                }
                .free-postage {
                  position: absolute;
                  top: 0;
                  right: 0;
                  margin: 0;
                  padding: 0;
                  width: 50px;
                  color: #877a73;
                  box-shadow: none;
                }
              }
              .commodity-card-foot {
                // padding: 20px 0;
                display: flex;
                justify-content: space-between;
                align-items: center;
                .left {
                  color: #fa585a;
                  font-size: 25px;
                }
              }
            }
          }
        }
      }
    }
  }
</style>
