<template>
  <li class="product-card">
    <div class="pic">
      <img src="https://img.alicdn.com/bao/uploaded/i2/2207686621837/O1CN01d4Q4Zg1PROETEv1Uc_!!0-item_pic.jpg"
           alt="car-img">
    </div>
    <div class="msg">
      <div class="title">老虎积雪草修护面膜补水保湿紧致控油收缩毛孔男女士官方正品韩国</div>
      <div class="card-keywords">
        <span class="keyword tmall">天猫</span>
        <span class="keyword">大额卷</span>
        <span class="keyword free-postage">包邮</span>
      </div>
      <div class="card-foot">
        <div class="price">
          <span class="price-tag">￥</span>
          <span class="price-strong">9</span>
          <span class="digit">.9</span>
        </div>
        <div class="info">4.3万人已买</div>
        <div class="coupon-value">80元卷</div>
      </div>
    </div>
  </li>
</template>

<style lang="scss">
  .product-card {
    width: 276px;
    height: 390px;
    margin: 10px 11px;
    list-style: none;
    cursor: pointer;
    background: #fff;
    box-shadow: 0 1px 0px -1px rgba(0,0,0,.3);
    &:hover {
      box-shadow: 0 5px 10px -1px rgba(0,0,0,.3);
      transition-duration: 1s;
    }
    .pic {
      width: 276px;
      height: 276px;
      img {
        width: 100%;
        height: 100%;
      }
    }
    .msg {
      padding: 0 10px;
      .title {
        width: 100%;
        height: 50px;
        font-size: 14px;
        color: #877a73;
        line-height: 50px;
        overflow: hidden;
        text-overflow: ellipsis;
        white-space: nowrap;
      }
      .card-keywords {
        overflow: hidden;
        position: relative;
        .keyword {
          float: left;
          box-sizing: border-box;
          margin: 0 6px 0 0;
          padding: 0 6px;
          min-width: 40px;
          font-size: 14px;
          color: #ff9000;
          line-height: 20px;
          vertical-align: middle;
          text-align: center;
          border-radius: 2px;
          box-shadow: inset 0 0 0 1px #ff9000;
        }
        .tmall {
          color: #fff;
          border-radius: 2px;
          background-color: #df2b2f;
          box-shadow: none;
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
      .card-foot {
        margin-top: 14px;
        height: 28px;
        position: relative;
        display: flex;
        .price {
          color: #fa585a;
          font-size: 0;
          font-weight: 400;
          line-height: 1;
          margin-right: 6px;
          vertical-align: bottom;
          .price-tag {
            display: inline-block;
            font-size: 12px;
            font-style: normal;
            font-weight: 400;
          }
          .price-strong {
            display: inline-block;
            font-size: 28px;
          }
          .digit {
            display: inline-block;
            font-size: 18px;
          }
        }
        .info {
          font-size: 14px;
          color: #877a73;
          letter-spacing: 0;
          line-height: 30px;
        }
        .coupon-value {
          font-size: 12px;
          margin-top: 4px;
          padding: 0 5px;
          position: absolute;
          right: 0;
          color: #fa585a;
          border-radius: 2px;
          box-shadow: inset 0 0 0 1px #fa585a;
        }
      }
    }
  }
</style>
