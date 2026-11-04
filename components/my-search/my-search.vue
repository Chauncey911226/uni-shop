<template>
	<view class="my-search-container" :style="{'background-color':bgcolor}" @click="searchBoxHandler">
		<view class="my-search-box" :style="{'border-radius':radius+'px'}">
			<uni-icons type="search" size="20"></uni-icons>
			<text class="placeholder">搜索</text>
		</view>
	</view>
</template>

<script>
	import uniIcons from "@/uni_modules/uni-icons/components/uni-icons/uni-icons.vue"
	export default {
	  name:"my-search",
	  components:{
		uniIcons
	  },
	  data() {
		return {};
	  },
	  props:{
		  bgcolor:{
			  type:String,
			  default:"#C00000"
		  },
		  radius:{
			  type:Number,
			  default:18
		  }
	  },
	  methods:{
		  searchBoxHandler(){
			  this.$emit('click')
		  }
	  }
	}
</script>

<style lang="scss">
	.my-search-container {
		height: 50px;
		// background-color: #c00000;
		display: flex;
		align-items: center;
		padding: 0 10px;
		.my-search-box {
			height: 36px;
			background-color: #fff;
			// border-radius: 18px;
			width: 100%;
			display: flex;
			align-items: center;
			justify-content: center;
			.placeholder {
				font-size: 15px;
				margin-left: 5px;
			}
		}
	}
</style>
