<template lang="html">
    <Panel :class="$style.panel" title="理财精选">
        <section :class="$style.content">
            <dl v-for="item in items" :class="$style.item" :key="item.title">
                <dt> {{ item.title }} <span>{{ item.sub }}</span></dt>
                <dd>{{ item.rate }}</dd>
                <dd>{{ item.text }}</dd>
            </dl>
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
                title: "定期理财",
                sub: "理财首选",
                rate: "5.6%",
                text: "历史年化回报率",
            }, {
                title: "小白理财",
                sub: "理财首选",
                rate: "4.22%",
                text: "7日年化收益率",
            }, {
                title: "月月盈",
                sub: "养老保障",
                rate: "5%",
                text: "7日年化收益率",
            }, {
                title: "小白基金",
                sub: "天天赚钱",
                rate: "4.27%",
                text: "7日年化收益率",
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
      &::after {
        //!important 技巧点-中间的线
        content:"";
        display: block;
        width: 100%;
        height: 0px;
        box-sizing: border-box;
        border-bottom: 1px solid rgb(187, 141, 141);
        position: relative;
        top:-195px;
      }
      @include flex(row);
      justify-content: space-around;
      box-sizing: border-box;
      .item {
        position: relative;
        width: 50%;
        padding: 34px 16px;
        box-sizing: border-box;
        &::after {
          //!important 技巧点-右边的线
          content:"";
          width: 1px;
          height: 136px;
          display: block;
          position: absolute;
          top: 5%;
          right: 0;
          margin-top: 20px;
          border-right: 1px solid rgb(187, 141, 141);
        }
        &:nth-child(2n) {
          &::after {
            display: none;
          }
        }
        dt {
          font-size: 30px;
          line-height: 32px;
          color: #333;
          span {
            font-size: 22px;
            color: #ff5155;
            border: 1px solid #ff5155;
            padding: 0 8px;
            vertical-align: 1px;
          }
        }
        dd {
          &:nth-child(2) {
            font-weight: 700;
            font-size: 44px;
            height: 58px;
            line-height: 58px;
            color: #ff5155;
            white-space: nowrap;
            text-overflow: ellipsis;
            overflow: hidden;
          }
          &:nth-child(3) {
            font-size: 24px;
            height: 34px;
            line-height: 34px;
            color: #999;
            white-space: nowrap;
            text-overflow: ellipsis;
            overflow: hidden;
          }
        }
      }
    }
  }
</style>
