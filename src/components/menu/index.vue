<template>
  <div>
    <div class="nav-body">
      <!-- 侧边导航 -->
      <div class="nav-side" ref="navSide" @mouseleave="hideDetail">
        <ul>
          <li @mouseenter="showDetail">
            <span class="nav-side-item">女装</span> /
            <span class="nav-side-item">女鞋</span>
          </li>
          <li @mouseenter="showDetail" >
            <span class="nav-side-item">男装</span> /
            <span class="nav-side-item">男鞋</span>
          </li>
          <li @mouseenter="showDetail">
            <span class="nav-side-item">美妆</span> /
            <span class="nav-side-item">个护</span>
          </li>
          <li @mouseenter="showDetail">
            <span class="nav-side-item">配饰</span> /
            <span class="nav-side-item">箱包</span> 
          </li>
          <li @mouseenter="showDetail">
            <span class="nav-side-item">零食王国</span> 
          </li>
          <li @mouseenter="showDetail">
            <span class="nav-side-item">母婴用品</span> 
          </li>
          <li @mouseenter="showDetail">
            <span class="nav-side-item">手机</span> /
            <span class="nav-side-item">数码</span> 
          </li>
          <li @mouseenter="showDetail">
            <span class="nav-side-item">内衣袜子</span>
          </li>
          <li @mouseenter="showDetail">
            <span class="nav-side-item">文娱</span> /
            <span class="nav-side-item">家居</span>

          </li>
        </ul>
    <transition name="fade">
      <div class="detail-item-panel panel-2" :duration="{ enter: 100, leave: 200 }" v-show="panel1" @mouseenter="showDetail" ref="itemPanel" @mouseleave="hideDetail">
        <div class="nav-detail-item">
          <span v-for="(item, index) in panelData1.navTags" :key="index">{{item}} > </span>
        </div>
        <ul>
          <li v-for="(items, index) in panelData1.classNav" :key="index" class="detail-item-row">
            <span class="detail-item-title">{{items.title}}
              <span class="glyphicon glyphicon-menu-right"></span>
            </span>
            <router-link to="/goodsList" v-for="(item, subIndex) in items.tags" :key="subIndex">
              <span class="detail-item">{{item}}</span>
            </router-link>
          </li>
        </ul>
      </div>
    </transition>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeNav',
  data () {
    return {
      panel1: false,
      panel2: false,
      nav: [
        '秒杀',
        '优惠券',
        '闪购',
        '拍卖',
        '服装城',
        '超市',
        '生鲜',
        '全球购',
        '金融'
      ],
      panelData1: {
        navTags: [ '女装' ],
        classNav: [
          {
            title: '女装',
            tags: [ '本周上新','韩系少女','衬衫马甲','T恤外套','卫衣','连衣裙','半身裙','裤装' ]
          }
        ]
      },
    };
  },
  methods: {
    showDetail () {
      this.panel1 = true;
    },
    hideDetail () {
      this.panel1 = false;
    }
  },
  mounted () {
    this.$refs.itemPanel.style.left = this.$refs.navSide.offsetLeft + this.$refs.navSide.offsetWidth + 'px';
    this.$refs.itemPanel.style.top = this.$refs.navSide.offsetTop + 'px';
  },
  updated () {
    this.$refs.itemPanel.style.left = this.$refs.navSide.offsetLeft + this.$refs.navSide.offsetWidth + 'px';
    this.$refs.itemPanel.style.top = this.$refs.navSide.offsetTop + 'px';
  }
  // store
};
</script>

<style scoped>
/*大的导航信息，包含导航，幻灯片等*/
/* .nav-body {
  width: 1020px;
  height: 485px;
  margin: 0px auto;
} */
.nav-side {
  width: 220px;
  height: 370px;
  padding: 0px;
  color: #000;
  float: left;
  background-color: #fcf9e3;
}
.nav-side ul {
  width: 100%;
  padding: 0px;
  padding-top: 15px;
  list-style: none;
}
.nav-side li {
  padding: 7.5px;
  padding-left: 15px;
  font-size: 14px;
  line-height: 18px;
}
.nav-side li:hover {
  background: #999395;
}
.nav-side-item:hover {
  cursor: pointer;
  color: #c81623;
}

/*导航内容*/
.nav-content {
  width: 792px;
  margin-left: 15px;
  overflow: hidden;
  float: left;
}
/*导航图片*/
.nav-show-img {
  margin-top: 10px;
  float: left;
}
.nav-show-img:nth-child(2) {
  margin-left: 12px;
}
/*显示商品*/
.content {
  width: 100%;
}
/*显示商品详细信息*/
.detail-item-panel {
  width: 300px;
  height: 370px;
  background-color: #fff;
  position: absolute;
  top: 168px;
  left: 389px;
  z-index: 999;
}
.nav-detail-item {
  margin-left: 26px;
  margin-top: 15px;
  margin-bottom: 15px;
  cursor: pointer;
  color: #eee;
}
.nav-detail-item span {
  padding: 6px;
  padding-left: 12px;
  margin-left: 15px;
  font-size: 12px;
  background-color: #6e6568;
}
.nav-detail-item span:hover {
  margin-left: 15px;
  background-color: #f44336;
}
.detail-item-panel ul {
  list-style: none;
}
.detail-item-panel li {
  line-height: 38px;
  margin-left: 40px;
}
.detail-item-title {
  padding-right: 6px;
  font-weight: bold;
  font-size: 12px;
  cursor: pointer;
  color: #555555;
}
.detail-item-title:hover {
  color: #d9534f;
}
.detail-item-row a {
  color: #555555;
}
.detail-item{
  font-size: 14px;
  padding-left: 12px;
  padding-right: 8px;
  cursor: pointer;
  border-left: 1px solid #ccc;
}
.detail-item:hover {
  color: #d9534f;
}
</style>
