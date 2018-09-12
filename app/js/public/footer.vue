<template lang="html">
    <Panel :class="$style.panel">
        <ul :class="[$style.content,cname]">
            <li>
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t2842/350/3035567089/14791/5f6ff93d/577cf395N31e76288.png?width=1125&height=252">
            </li>
            <li>
                <div id="client-img">
                    <img src="//img12.360buyimg.com/jrpmobile/jfs/t2971/333/1297567079/898/f2d2e00d/577dc28dNe5138337.png?width=108&height=108">
                    <p>客户端</p>
                </div>
                <div id="client-img">
                    <img src="//img12.360buyimg.com/jrpmobile/jfs/t2824/256/2966087355/831/188bfa25/577cf3dcN18aadbf2.png?width=108&height=108">
                    <p>触摸版</p>
                </div>
                <div id="client-img">
                    <img src="//img12.360buyimg.com/jrpmobile/jfs/t2920/282/1283157010/1040/23f1430b/577cf3e5N53f740b8.png?width=108&height=108">
                    <p>电脑版</p>
                </div>
            </li>
            <li>Copyright © 2004-2018 京东JD.com 版权所有</li>
            <li>投资有风险，购买需谨慎</li>
            <li>京东金融平台服务协议</li>
            <li>京东金融隐私政策</li>
        </ul>
    </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
export default {
    components: {
        Panel,
    },
    props: {
        cname: {
            type: String,
            default: "",
        },
    },
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
  .panel {
    @include panel;
    h4 {
      display: none;
    }
    margin-bottom: 100px;
  }

  .content {
    background-color: #f5f5f5;
    li {
      display: block;
      text-align: center;
      color: #999;
      font-size: 24px;
      &:nth-child(n+3) {
        padding: 24px 0;
        height: 38px;
        line-height: 38px;
        border-top: 1px solid #ddd;
      }
      img {
        height: 143px;
        width: 100%;
      }
      &:nth-child(2) {
        @include flex(row);
        height: 186px;
        div {
          text-align: center;
          width: 33.3%;
          padding-top:20px;
          img {
            height: 90px;
            width:90px;
          }
          p {
            font-size: 26px;
            display: block;
            color: #999;
            white-space: nowrap;
            text-overflow: ellipsis;
            overflow: hidden;
            display: block;
            margin-top: 12px;
          }
        }
      }
    }
  }
</style>
