<template>
    <Panel :class="$style.panel" title="金融头条" style="margin-top:120px;">
        <section :class="$style.content">
            <swiper :options="swiperOption">
                <swiper-slide :class="$style.swiperSlide">签到领流量，1元500M <em>></em></swiper-slide>
                <swiper-slide :class="$style.swiperSlide">百万白条券免费送，速来领取！! <em>></em></swiper-slide>
            </swiper>
        </section>
    </Panel>
</template>

<script>
import { swiper, swiperSlide } from "vue-awesome-swiper"
import Panel from "../core/panel.vue"
export default {
    components: {
        Panel,
        swiperSlide,
        swiper,
    },
    data() {
        return {
            swiperOption: {
                direction: "vertical",
                autoplay: true,
                loop: true,
            },
        }
    },
}
</script>

<style lang="scss">
  .swiper-container {
    height: 72px;
    overflow: hidden;
  }
</style>


<style lang="scss" module>
  @import "../../css/element.scss";
  .panel {
    @include panel;
    >h4 {
      display: none;
    }
    .content {
      height: 72px;
      line-height: 72px;
      overflow: hidden;
      padding-left: 178px;
      background: url(//m.jr.jd.com/spe/qyy/main/images/scroll_title_img.png) no-repeat left center;
      .swiperSlide {
        color: #333;
        font-size: 28px;
        font-family: PingFangSC-Medium;
        text-overflow: ellipsis;
        white-space: nowrap;
        overflow: hidden;
        em {
          color: #ddd;
          float: right;
          margin-right: 20px;
        }
      }
    }
  }
</style>


