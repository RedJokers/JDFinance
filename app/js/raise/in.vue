<template>
    <Panel :class="$style.panel" title="In货推荐">
        <section :class="$style.content">
            <div v-for="item in items" :class="$style.item" :key="item.catory">
                <img :src="item.catory">
                <div v-for="product in item.list" :class="$style.list" :key="product.img">
                    <div :class="$style.product" >
                        <img :src="product.img">
                        <p :class="$style.title">{{ product.title }}</p>
                        <p :class="$style.price"> <em> {{ product.price }}</em>起</p>
                        <article :class="$style.progressBar">
                            <div :class="$style.wrapper">
                                <div :class="$style.inner" :style="{width:product.progress}"/>
                            </div>
                            <p>{{ product.progress }}%</p>
                        </article>
                    </div>
                </div>
            </div>
        </section>
    </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
export default {
    components: {
        Panel,
    },
    data() {
        return {
            items: [{
                catory: "//img12.360buyimg.com/jrpmobile/jfs/t3406/210/2247820735/50952/86016eea/5846d8e7N20446dbd.png?width=750&height=200",
                list: [{
                    img: "//img30.360buyimg.com/cf/s250x250_jfs/t16897/179/5503620/136988/48118941/5a57290bN52e19f82.jpg",
                    title: "微型摄像头",
                    price: "49.00",
                    progress: 55,
                }, {
                    img: "//img30.360buyimg.com/cf/s250x250_jfs/t19180/119/103841930/89625/55994449/5a5d59f9N01432fde.jpg",
                    title: "智能手表",
                    price: "99.00",
                    progress: 84,
                }],
            }, {
                catory: "//img12.360buyimg.com/jrpmobile/jfs/t3739/82/2244582797/54399/746c7d79/5846a953N66b67d05.png?width=750&height=200",
                list: [{
                    img: "//img30.360buyimg.com/cf/s250x250_jfs/t13834/192/2625202072/70435/e5b85a62/5a460eefN94289190.jpg",
                    title: "智能后视镜",
                    price: "190.00",
                    progress: 120,
                }, {
                    img: "//img30.360buyimg.com/cf/s250x250_jfs/t17917/186/321392651/99329/32c1ae84/5a6c0e2cNdcabeb5c.jpg",
                    title: "REXL雾化电子烟",
                    price: "69.00",
                    progress: 35,
                }],
            }, {
                catory: "//img12.360buyimg.com/jrpmobile/jfs/t3214/113/4408032436/61548/ce316eef/5846d310Ne93f00c9.png?width=750&height=200",
                list: [{
                    img: "//img30.360buyimg.com/cf/s250x250_jfs/t17917/186/321392651/99329/32c1ae84/5a6c0e2cNdcabeb5c.jpg",
                    title: "雪花酥",
                    price: "29.00",
                    progress: 77,
                }, {
                    img: "//img30.360buyimg.com/cf/s250x250_jfs/t14506/168/2096353267/153845/5bb0a2e6/5a6e9518N15da6f7c.jpg",
                    title: "中秋月饼",
                    price: "79.00",
                    progress: 230,
                }],
            }],
        }
    },
}
</script>

<style lang="scss" module>
  @import "../../css/element.scss";
  .panel {
    @include panel;
    .content {
      @include flex;
      box-sizing: border-box;
      .item {
        @include flex(row);
        margin-bottom: 40px;
        >img {
          display: block;
          width: 100%;
          height: 170px;
        }
        .list {
          width: 50%;
          .product {
            width: 100%;
            height: 396px;
            box-sizing: border-box;
            background: rgba(0,0,0,.02);
            text-align: center;
            img {
              width: 180px;
              height: 180px;
              margin: 44px auto 20px;
            }
            .title {
              font-size: 28px;
              font-family: PingFangSC-Medium;
              color: #444;
            }
            .price {
              font-size: 20px;
              color: #999;
              font-family: PingFangSC-Medium;
              line-height: 48px;
              height: 48px;
              em {
                margin-right: 4px;
                color: #ff3232;
                font-size: 36px;
                &::before {
                  content: "￥";
                  font-size: 28px;
                }
              }
            }
            .progress-bar {
              @include flex(row);
              align-items: center;
              justify-content: space-around;
              padding: 0 20px;
              height: 30px;
              line-height: 30px;
              margin-top: 16px;
              .wrapper {
                height: 10px;
                width: 144px;
                border-radius: 22px;
                background: #f6e6e6;
                .inner {
                  width: 40%;
                  max-width: 100%;
                  height: 10px;
                  background: linear-gradient(to left,#f55 1%,#ff9c31 100%);
                  border-radius: 22px;
                }
              }
              >p {
                font-size: 24px;
                color: #999;
              }
            }
          }
        }
      }
    }
  }
</style>

