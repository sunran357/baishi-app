<template>
  <view class="home">
    <view class="list-view-container">
		<view class="list-wrapper">
			<view class="img-li"></view>
			<view>
				<text class="name">2021 新年日程计划</text>
				<text class="describe">2021新年计划，牛年大吉！…</text>
			</view>
		</view>
	</view>
  </view>
</template>
<script>
import './index.scss'
export default {
  name: "Home",
  data() {
    return {
      dataList: [
        {
          image: require("../../assets/image/livingRoom.jpg"),
          tipsList: [
            {
              position: { x: -200, y: -4, z: -147 },
              content: {
                title: "进入厨房",
                text: "",
                image: 1,
                showTip: false,
                showTitle: true,
              },
            },
          ],
        },
      ],
      tooltopContent: {},
    };
  },
  methods: {
    
    initCamera(element) {
     
    },
    
    initContent(index = 0) {
      
    },
    
  },
  mounted() {
    
  },
  destroyed() {
  },
};
</script>

<style lang="scss" scoped>
.home {
  position: relative;
  width: 100%;
  height: 100%;
  overflow: hidden;
  .view-container {
    width: 100%;
    height: 100%;
    overflow: hidden;
  }
  .title-text {
    position: absolute;
    width: 66px;
    color: #382129;
  }
  .tooltip-box {
    position: absolute;
    padding: 0px 0px 40px 0px;
    line-height: 30px;
    border-radius: 4px;
    color: #ffffff;
    z-index: 100;
    cursor: pointer;
    .container {
      position: relative;
      width: 240px;
      max-height: 200px;
      padding: 10px;
      background-color: rgba(0, 0, 0, 0.6);
      // &::before {
      //   content: "";
      //   position: absolute;
      //   bottom: -16px;
      //   left: 20%;
      //   border-top: 16px solid rgba(0, 0, 0, 0.8);
      //   border-left: 10px solid transparent;
      //   border-right: 10px solid transparent;
      // }
      .title {
        width: 100%;
        padding: 6px 0;
      }
      .explain {
        width: 100%;
        max-height: 100px;
        font-size: 14px;
        overflow-y: auto;
        &::-webkit-scrollbar {
          width: 4px;
          height: 4px;
        }
        &::-webkit-scrollbar-track {
          background: #353535;
          border-radius: 2px;
        }
        &::-webkit-scrollbar-thumb {
          background: #cdcdcd;
          border-radius: 2px;
        }
        &::-webkit-scrollbar-thumb:hover {
          background: #9c9c9c;
        }
        &::-webkit-scrollbar-corner {
          background: #f6f6f6;
        }
      }
    }
  }
}
</style>