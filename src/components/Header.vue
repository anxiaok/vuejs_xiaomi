<template>
  <header>
      <div class="container">
          <div class="topbar-nav">
              <router-link to="//www.mi.com/index.html">小米商城</router-link><span class="sep">|</span>
              <router-link to="https://www.miui.com/"  target="_blank">MIUI</router-link><span class="sep">|</span>
              <router-link to="https://iot.mi.com/index.html" target="_blank">IoT</router-link><span class="sep">|</span>
              <router-link to="https://i.mi.com/" target="_blank">云服务</router-link><span class="sep">|</span>
              <router-link to="https://shuidi.mi.com/" target="_blank">水滴</router-link><span class="sep">|</span>
              <router-link to="https://jr.mi.com?from=micom" target="_blank">金融</router-link><span class="sep">|</span>
              <router-link to="https://youpin.mi.com/" target="_blank">有品</router-link><span class="sep">|</span>
              <router-link to="//www.mi.com/index.html" target="_blank">Select Region</router-link>
          </div>
          <div class="topbar-cart" :class="{'active':isActive}" @mouseover="show" @mouseout="show">
              <router-link to="//static.mi.com/cart/" class="cart-mini">
                <i class="iconfont icon-gouwuchekong"></i>购物车<span class="cart-mini-num">（0）</span>
              </router-link>
            <div class="cart-menu" :class="{'active':isActive}">
                <div class="loading">购物车中还没有商品，赶紧选购吧！</div>
            </div>
        </div>
        <div class="topbar-info">
            <router-link class="link" target="_blank" to="//order.mi.com/site/login?redirectUrl=https://www.mi.com/?client_id=180100041086&amp;masid=17489.0001">登录</router-link><span class="sep">|</span>
            <router-link class="link" target="_blank"  to="https://account.xiaomi.com/pass/register">注册</router-link><span class="sep">|</span>
            <span class="message">
                <router-link to="//order.mi.com/message/list">
                    消息通知<i class="J_miMessageTotal"></i>
                </router-link>
            </span>
      </div>
      </div>
  </header>
</template>
<script>
import "../assets/css/iconfont.css";
export default {
  name: "Header",
  data() {
    return {
      isActive: false
    };
  },
  methods: {
    show() {
      this.isActive = !this.isActive;
    }
  }
};
</script>
<style lang="less" scoped>
* {
  margin: 0;
  padding: 0;
}
a {
  text-decoration: none;
  &:hover {
    color: #fff;
  }
}
header {
  position: relative;
  z-index: 30;
  height: 40px;
  font-size: 12px;
  color: #b0b0b0;
  background: #333;
  .container {
    width: 1226px;
    margin-right: auto;
    margin-left: auto;
    &:before,
    &:after {
      content: " ";
      display: table;
    }
    .topbar-nav {
      float: left;
      height: 40px;
      line-height: 40px;
      overflow: hidden;
      _zoom: 1;
      a {
        color: #b0b0b0;
        text-decoration: none;
        &:hover {
          color: #fff;
        }
      }
      .sep {
        margin: 0 0.5em;
        color: #424242;
        font-family: sans-serif;
      }
    }

    .topbar-cart,
    .topbar-info {
      position: relative;
      float: right;
      _display: inline;
      height: 40px;
    }
    .topbar-cart {
      width: 120px;
      margin-left: 15px;
      .cart-mini {
        position: relative;
        z-index: 32;
        display: block;
        height: 40px;
        line-height: 40px;
        text-align: center;
        color: #b0b0b0;
        background: #424242;
        i {
          margin-right: 4px;
          font-size: 20px;
          line-height: 20px;
          vertical-align: -4px;
        }
        &-num {
          margin-left: -4px;
        }
      }
      .cart-menu {
        display: none;
        position: absolute;
        right: 0;
        right: -1px;
        top: 40px;
        z-index: 31;
        width: 316px;
        padding: 15px 0 0;
        color: #424242;
        background: #fff;
        border: 1px solid #e0e0e0;
        border-top: 0;
        -webkit-box-shadow: 0 2px 10px rgba(0, 0, 0, 0.15);
        box-shadow: 0 2px 10px rgba(0, 0, 0, 0.15);
        .loading {
          margin: 5px 20px 20px;
          text-align: center;
          padding: 20px 0;
        }
      }
    }
    .active {
      .cart-mini {
        color: #ff6700;
        background: #fff;
      }
      .cart-menu {
        display: block;
      }
    }
    .topbar-info {
      line-height: 40px;
      a {
        color: #b0b0b0;
        &:hover {
          color: #fff;
        }
      }
      .link {
        padding: 0 5px;
        text-align: center;
      }
      .link,
      .user,
      .message,
      .sep {
        float: left;
      }
      .sep {
        color: #424242;
      }
      .message {
        padding: 0 10px;
      }
    }
  }
}
</style>
