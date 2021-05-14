<template>
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
           src="@/assets/images/code.png"
           alt="">
    </div>
  </div>

</template>

<style lang="scss" scoped>
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
</style>