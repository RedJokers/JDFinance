<template>
    <Panel :class="$style.panel" title="白条福利">
        <section>
            <div :class="$style.item">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t4378/62/155957680/9017/16463551/58affd58Nb5c9198e.jpg?width=120&height=120">
                <div>
                    <p>开通白条</p>
                    <p>送188元礼包</p>
                </div>
                <em>立即开通 ></em>
            </div>
            <div :class="$style.item">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t4150/330/141981421/9147/604e3e04/58affc3bNbfa8f9d7.jpg?width=120&height=120">
                <div>
                    <p>白条闪付</p>
                    <p>新手享158元礼包</p>
                </div>
                <em>随机立减 ></em>
            </div>
            <div :class="$style.item">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t4270/96/1102370053/8651/58b7fa5a/58bd2e10N453e9464.jpg?width=120&height=120">
                <div>
                    <p>白条提额</p>
                    <p>金融APP专享提额礼包</p>
                </div>
                <em>去提额 ></em>
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
    .item {
      @include flex(row);
      align-items: center;
      height: 140px;
      &::before {
        content: '';
        display: block;
        width: 100%;
        height: 0;
        border: 0.5px solid #ddd;
      }
      &:last-child::after {
        content: '';
        display: block;
        width: 100%;
        height: 0;
        border: 0.5px solid #ddd;
      }
      img {
        width: 88px;
        height: 88px;
        margin: 0 32px;
      }
      div {
        p {
          line-height: 1.8;
          font-size: 32px;
          width: 344px;
          white-space: nowrap;
          text-overflow: ellipsis;
          overflow: hidden;
          &:last-child {
            line-height: 1.1;
            font-size: 24px;
            color: #999;
            white-space: nowrap;
            text-overflow: ellipsis;
            overflow: hidden;
            }
        }
      }
      em {
        color: #FF801A;
        font-size: 28px;
      }
    }
  }
</style>

