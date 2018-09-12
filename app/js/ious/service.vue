<template>
    <Panel :class="$style.panel" title="更多服务">
        <section :class="$style.content">
            <div :class="$style.item">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t4609/245/3975151339/11019/766e751d/590aca78Nf15a7947.png?width=135&height=135">
                <p>大王卡</p>
            </div>
            <div :class="$style.item">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t8311/300/1385281399/9501/130a0046/59b8da06N14f62cf3.png?width=120&height=120">
                <p>借钱</p>
            </div>
            <div :class="$style.item">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t5095/216/1045040184/12370/564ae632/590ac7deN9a0eac2a.png?width=135&height=135">
                <p>消费分期</p>
            </div>
            <div :class="$style.item">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t5269/224/1031852465/12646/40e0f799/590aca55N22a6f274.png?width=135&height=135">
                <p>白条商城</p>
            </div>
            <div :class="$style.item">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t19825/175/2716312753/5076/dfe2d74f/5b7cc241N65ff1885.png?width=90&height=90">
                <p>领红包</p>
            </div>
            <div :class="$style.item">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t24682/140/813231673/5159/f8133cd6/5b7cc24fNb15a2746.png?width=90&height=90">
                <p>福利</p>
            </div>
            <div :class="$style.item">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t24289/19/2403404444/4856/13f8bcb9/5b7cc264Nb9e090f2.png?width=90&height=90">
                <p>抽奖</p>
            </div>
            <div :class="$style.item">
                <img src="http://img12.360buyimg.com/jrpmobile/jfs/t5371/323/1038197138/12031/3ec72f6c/590aca20N089fd34a.png?width=135&height=135">
                <p>钢镚</p>
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
}
</script>

<style lang="scss" module>
  @import "../../css/element.scss";
  .panel {
    @include panel;
    .content {
      @include flex(row);
      .item {
        width: 25%;
        margin-bottom: 40px;
        img {
          width: 90px;
          height: 90px;
          display: block;
          margin: 0 auto;
        }
        p {
          font-size: 26px;
          color: #666;
          margin-top: 12px;
          text-align: center;
        }
      }
    }
  }
</style>

