<template>
  <div class="swiper-container mySwiper">
    <div class="swiper-wrapper">
      <div class="swiper-slide">
        <img src="https://img1.lukou.com/static/coupon/p/image_link/JiV6OeaUX4jPoJwOozMLBWq2JHV2NkAd.png" alt="1">
      </div>
      <div class="swiper-slide">
        <img src="https://img1.lukou.com/static/coupon/p/image_link/0AYtSEEZSOB3xIHf6OUVfEsspjdOwqYZ.png" alt="22">
      </div>
    </div>
    <div class="swiper-pagination"></div>
    <div class="swiper-button-prev swiper-button-white ">

    </div><!--左箭头。如果放置在swiper-container外面，需要自定义样式。-->
    <div class="swiper-button-next swiper-button-white ">
    </div><!--右箭头。如果放置在swiper-container外面，需要自定义样式。-->
  </div>
</template>

<script>

import Swiper from 'swiper'

export default {
  data() {
    return {
      mySwiper: null
    };
  },
  computed: {},
  mounted() {
    this.mySwiper = new Swiper('.mySwiper', {
      // 播放指示
      pagination: {
        el: ".swiper-pagination",
      },
      autoplay: true, // 自动播放
      loop: true,  // 循环
      // 切换按钮
      navigation: {
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev',
      },
    })

//鼠标移出隐藏按钮，移入显示按钮
    this.mySwiper.el.οnmοuseοver = function () { // 鼠标经过事件
      this.mySwiper.navigation.$nextEl.removeClass('hide');
      this.mySwiper.navigation.$prevEl.removeClass('hide');
    }
    this.mySwiper.el.οnmοuseοut = function () { // 鼠标移出事件
      this.mySwiper.navigation.$nextEl.addClass('hide');
      this.mySwiper.navigation.$prevEl.addClass('hide');

    }
  }
}
</script>

<style>
.swiper-container {
  width: 100%;
  height: 100%;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: #fff;

  /* Center slide text vertically */
  display: -webkit-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  -webkit-justify-content: center;
  justify-content: center;
  -webkit-box-align: center;
  -ms-flex-align: center;
  -webkit-align-items: center;
  align-items: center;
}

.swiper-slide img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.my-button:after {
  content: '';
}
.pagination-img {
  width: 27px;
  height: 30px;

}

.hide {
  opacity: 0;
}

.swiper-button-next, .swiper-button-prev {
  transition: opacity .5s;
}
</style>
