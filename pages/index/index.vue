<template>
	<view class="content">
		<!-- 头部 -->
		<view class="navbar">
			<view v-for="(item, index) in navList" :key="index" class="nav-item" :class="{ current: tabCurrentIndex === index }" @click="tabClick(index)">
				{{ item.text }}
			</view>
		</view>
		<!-- 显示区域 -->
		<view class="list" v-for="(item, index) in navList" :key="index" v-if="tabCurrentIndex === index">		
			<view class="box">
				<view class="head">
					<view>
						<image style="width: 16px;" mode="widthFix" src="../../static/sc.png" ></image>
						cdf会员购北京
						<image style="width: 16px;" mode="widthFix" src="../../static/you.png" ></image>
					</view>
					<view class="status">{{item.text}}</view>
				</view>
					<view class="content2">
						<view><image class="goods-img" src="../../static/dn.png" mode="widthFix"></image></view>
						<view class="right">
							<view class="title">
								<text>肌肤之月光灵前霜  37Mlx2</text>
								<text class="price">￥178.00</text>
							</view>
							<view class="gray">创建订单时间：2020-09-01 17:22:03</view>
							<view class="gray">创建订单时间：2020-09-01 17:22:03</view>
							<view class="gray">支付时间<text class="gopay">去支付订单</text></view>							
						</view>
					</view>
					<view class="btns">
						<view class="btn1">再来一单</view>
						<view class="btn2">分享得500积分</view>
					</view>		
			</view>
			
			<view class="box">
				<view class="head">
					<view>
						<image style="width: 16px;" mode="widthFix" src="../../static/sc.png" ></image>
						cdf会员购北京
						<image style="width: 16px;" mode="widthFix" src="../../static/you.png" ></image>
					</view>
					<view class="status">{{item.text}}</view>
				</view>
					<view class="content2">
						<view><image class="goods-img" src="../../static/dn.png" mode="widthFix"></image></view>
						<view class="right">
							<view class="title">
								<text>肌肤之月光灵前霜  37Mlx2</text>
								<text class="price">￥178.00</text>
							</view>
							<view class="gray">创建订单时间：2020-09-01 17:22:03</view>
							<view class="gray">创建订单时间：2020-09-01 17:22:03</view>
							<view class="gray">支付时间<text class="gopay">去支付订单</text></view>							
						</view>
					</view>
					<view class="btns">
						<view class="btn1">再来一单</view>
						<view class="btn2">分享得500积分</view>
					</view>		
			</view>
			
			<view class="box">
				<view class="head">
					<view>
						<image style="width: 16px;" mode="widthFix" src="../../static/sc.png" ></image>
						cdf会员购北京
						<image style="width: 16px;" mode="widthFix" src="../../static/you.png" ></image>
					</view>
					<view class="status">{{item.text}}</view>
				</view>
					<view class="content2">
						<view><image class="goods-img" src="../../static/dn.png" mode="widthFix"></image></view>
						<view class="right">
							<view class="title">
								<text>肌肤之月光灵前霜  37Mlx2</text>
								<text class="price">￥178.00</text>
							</view>
							<view class="gray">创建订单时间：2020-09-01 17:22:03</view>
							<view class="gray">创建订单时间：2020-09-01 17:22:03</view>
							<view class="gray">支付时间<text class="gopay">去支付订单</text></view>							
						</view>
					</view>
					<view class="btns">
						<view class="btn1">再来一单</view>
						<view class="btn2">分享得500积分</view>
					</view>		
			</view>
			
			<view class="box">
				<view class="head">
					<view>
						<image style="width: 16px;" mode="widthFix" src="../../static/sc.png" ></image>
						cdf会员购北京
						<image style="width: 16px;" mode="widthFix" src="../../static/you.png" ></image>
					</view>
					<view class="status">{{item.text}}</view>
				</view>
					<view class="content2">
						<view><image class="goods-img" src="../../static/dn.png" mode="widthFix"></image></view>
						<view class="right">
							<view class="title">
								<text>肌肤之月光灵前霜  37Mlx2</text>
								<text class="price">￥178.00</text>
							</view>
							<view class="gray">创建订单时间：2020-09-01 17:22:03</view>
							<view class="gray">创建订单时间：2020-09-01 17:22:03</view>
							<view class="gray">支付时间<text class="gopay">去支付订单</text></view>							
						</view>
					</view>
					<view class="btns">
						<view class="btn1">再来一单</view>
						<view class="btn2">分享得500积分</view>
					</view>		
			</view>
		</view>
	</view>
</template>

<script>

export default {
	components: {
		
	},
	data() {
		return {
			tabCurrentIndex: 0,
			navList: [
				{
					state: 0,
					text: '全部',
					orderList: []
				},
				{
					state: 1,
					text: '待付款',
					orderList: []
				},
				{
					state: 2,
					text: '待收货',
					orderList: []
				},
				{
					state: 3,
					text: '待评价',
					orderList: []
				},
				{
					state: 4,
					text: '售后',
					orderList: []
				}
			]
		};
	},

	onLoad(options) {
		// 页面显示是默认选中第一个
		this.tabCurrentIndex = 0;
	},

	methods: {
		changeTab(e) {
			this.tabCurrentIndex = e.target.current;
		},
		//顶部tab点击
		tabClick(index) {
			this.tabCurrentIndex = index;
		}
	}
};
</script>

<style lang="scss">
.content {
	background: #f7f7f7;
	min-height: 100vh;
	font-size: 14px;
	padding-bottom: 40upx;
}
// box开始
.box{
	background: #fff;
	border-radius: 16upx;
	margin: 15px 15px 0;
	.head{
		padding: 15px;
		border-bottom: 1upx solid #f7f7f7;
		display: flex;
		justify-content: space-between;
		image{
			vertical-align: middle;
		}
		.status{
			color: $base-color;
		}
	}
	.content2{
		display:flex ;
		padding: 15px;
		.goods-img{
			width: 150upx;
			border-radius: 15upx;
			margin-right: 20upx;
		}
		.right{
			flex: 1;
			display: flex;
			flex-direction: column;
			justify-content: space-between;
			.title{
				display: flex;
				justify-content: space-between;
			}
			.price{
				font-weight: 600;
			}
			.gray{
				font-size: 12px;
				color: #9f9ea1;
				.gopay{
					background: #ffe8e4;
					color: $base-color;
					border-radius: 30upx;
					padding: 4upx 20upx;
					margin-left: 10upx;
				}
			}
		}
		
		
	}
	.btns{
		display: flex;
		justify-content: flex-end;
		padding: 15px;
		view{
			padding: 0 20upx;
			height: 50upx;
			line-height: 50upx;
			border-radius: 50upx;				
		}
		.btn1{
			color: #666464;
			border: 1px solid #666464;
			margin-right: 20upx;
		}
		.btn2{
			color: $base-color;
			border: 1px solid $base-color;
		}
	}
}
 
// box结束




.swiper-box {
	height: calc(100% - 40px);
}
.list-scroll-content {
	height: 100%;
}

.navbar {
	display: flex;
	height: 50px;
	padding: 0 5px;
	background: #fff;
	box-shadow: 0 1px 5px rgba(0, 0, 0, 0.06);
	position: relative;
	z-index: 10;
	.nav-item {
		flex: 1;
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100%;
		// font-size: 15px;
		font-weight: 600;
		color: $font-color-dark;
		position: relative;
		&.current {
			color: $base-color;
			&:after {
				content: '';
				position: absolute;
				left: 50%;
				bottom: 0;
				transform: translateX(-50%);
				width: 44px;
				height: 0;
				border-bottom: 3px solid $base-color;
			}
		}
	}
}

.uni-swiper-item {
	height: auto;
}
// .order-item {
// 	display: flex;
// 	flex-direction: column;
// 	padding-left: 30upx;
// 	background: #fff;
// 	margin-top: 16upx;
// 	.i-top {
// 		display: flex;
// 		align-items: center;
// 		height: 80upx;
// 		padding-right: 30upx;
// 		font-size: $font-base;
// 		color: $font-color-dark;
// 		position: relative;
// 		.time {
// 			flex: 1;
// 		}
// 		.state {
// 			color: $base-color;
// 		}
// 		.del-btn {
// 			padding: 10upx 0 10upx 36upx;
// 			font-size: $font-lg;
// 			color: $font-color-light;
// 			position: relative;
// 			&:after {
// 				content: '';
// 				width: 0;
// 				height: 30upx;
// 				border-left: 1px solid $border-color-dark;
// 				position: absolute;
// 				left: 20upx;
// 				top: 50%;
// 				transform: translateY(-50%);
// 			}
// 		}
// 	}
// 	/* 多条商品 */
// 	.goods-box {
// 		height: 160upx;
// 		padding: 20upx 0;
// 		white-space: nowrap;
// 		.goods-item {
// 			width: 120upx;
// 			height: 120upx;
// 			display: inline-block;
// 			margin-right: 24upx;
// 		}
// 		.goods-img {
// 			display: block;
// 			width: 100%;
// 			height: 100%;
// 		}
// 	}
// 	/* 单条商品 */
// 	.goods-box-single {
// 		display: flex;
// 		padding: 20upx 0;
// 		.goods-img {
// 			display: block;
// 			width: 120upx;
// 			height: 120upx;
// 		}
// 		.right {
// 			flex: 1;
// 			display: flex;
// 			flex-direction: column;
// 			padding: 0 30upx 0 24upx;
// 			overflow: hidden;
// 			.title {
// 				font-size: $font-base + 2upx;
// 				color: $font-color-dark;
// 				line-height: 1;
// 			}
// 			.attr-box {
// 				font-size: $font-sm + 2upx;
// 				color: $font-color-light;
// 				padding: 10upx 12upx;
// 			}
// 			.price {
// 				font-size: $font-base + 2upx;
// 				color: $font-color-dark;
// 				&:before {
// 					content: '￥';
// 					font-size: $font-sm;
// 					margin: 0 2upx 0 8upx;
// 				}
// 			}
// 		}
// 	}

// 	.price-box {
// 		display: flex;
// 		justify-content: flex-end;
// 		align-items: baseline;
// 		padding: 20upx 30upx;
// 		font-size: $font-sm + 2upx;
// 		color: $font-color-light;
// 		.num {
// 			margin: 0 8upx;
// 			color: $font-color-dark;
// 		}
// 		.price {
// 			font-size: $font-lg;
// 			color: $font-color-dark;
// 			&:before {
// 				content: '￥';
// 				font-size: $font-sm;
// 				margin: 0 2upx 0 8upx;
// 			}
// 		}
// 	}
// 	.action-box {
// 		display: flex;
// 		justify-content: flex-end;
// 		align-items: center;
// 		height: 100upx;
// 		position: relative;
// 		padding-right: 30upx;
// 	}
// 	.action-btn {
// 		width: 160upx;
// 		height: 60upx;
// 		margin: 0;
// 		margin-left: 24upx;
// 		padding: 0;
// 		text-align: center;
// 		line-height: 60upx;
// 		font-size: $font-sm + 2upx;
// 		color: $font-color-dark;
// 		background: #fff;
// 		border-radius: 100px;
// 		&:after {
// 			border-radius: 100px;
// 		}
// 		&.recom {
// 			background: #fff9f9;
// 			color: $base-color;
// 			&:after {
// 				border-color: #f7bcc8;
// 			}
// 		}
// 	}
// }
</style>
