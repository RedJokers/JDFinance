<template>
    <Panel :class="$style.panel" title="理财精选">
        <section :class="$style.content">
            <div :class="$style.item">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t3670/58/543125556/2606/a65096b9/580d80afN63b1085a.png?width=76&height=76">
                <div>
                    <p>月度理财</p>
                    <p>预计年化收益率4.50%</p>
                </div>
                <em>去赚钱 ></em>
            </div>
            <div :class="$style.item">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t3679/44/511862277/2728/c1c6b2bf/580d8189N6b6f8052.png?width=76&height=76">
                <div>
                    <p>季度理财</p>
                    <p>预计年化收益率5.50%</p>
                </div>
                <em>去赚钱 ></em>
            </div>
            <div :class="$style.item">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t3331/69/580199498/3074/d5bb21c5/580d7f6cN7f35e596.png?width=76&height=76">
                <div>
                    <p>一年理财</p>
                    <p>预计年化收益率5.50%</p>
                </div>
                <em>去赚钱 ></em>
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
    >h4 {
      border-bottom: 1px solid #ddd;
    }
    .content {
      @include flex;
      .item {
        @include flex(row);
        align-items: center;
        height: 140px;
        &::after {
          content: "";
          width: 100%;
          height: 0;
          border: 1px solid #ddd;
          box-sizing: border-box;
          margin-left: 150px;
        }
        &:last-child::after {
          border: 1px solid rgba(0, 0, 0, 0)
        }
        >img {
          width: 88px;
          height: 88px;
          margin: 0 32px;
        }
        p {
          font-size: 32px;
          color: #333;
          line-height: 1.8;
          width: 344px;
          white-space: nowrap;
          text-overflow: ellipsis;
          overflow: hidden;
          &:last-child {
            font-size: 24px;
            color: red;
            line-height: 1.2;
            white-space: nowrap;
            text-overflow: ellipsis;
            overflow: hidden;
          }
        }
        >em {
          color: #ff801a;
          font-size: 24px;
        }
      }
    }
  }
</style>
