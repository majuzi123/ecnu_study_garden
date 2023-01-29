<template>
	<view class="wholeContainer">
		<view class="">
			<Banner></Banner>
		</view>
		<view v-for="(actItem,index) in activityList" :key="index" class="activityItemContainer">
			<ActivityItem :actItem="actItem"></ActivityItem>
		</view>
	</view>
</template>

<script>
	import Banner from '../../components/IndexDiscover/Banner.vue'
	import ActivityItem from '../../components/Activity/ActivityItem.vue'
	export default {
		name:'activity',
		data() {
			return {
				activityList:[
					{
						id:'001',
						name:'活动一号',
						intro:'不要走在我的后面，因为我可能不会引路；不要走在我前面，因为我可能不会跟随；请走在我的身边，做我的朋友。——加缪',
						peopleNum:2000,
					},
					{
						id:'002',
						name:'活动二号',
						intro:'不要走在我的后面，因为我可能不会引路；不要走在我前面，因为我可能不会跟随；请走在我的身边，做我的朋友。——加缪',
						peopleNum:2001,
					},
					{
						id:'003',
						name:'活动三号',
						intro:'不要走在我的后面，因为我可能不会引路；不要走在我前面，因为我可能不会跟随；请走在我的身边，做我的朋友。——加缪',
						peopleNum:20,
					},
					{
						id:'004',
						name:'活动四号',
						intro:'不要走在我的后面，因为我可能不会引路；不要走在我前面，因为我可能不会跟随；请走在我的身边，做我的朋友。——加缪',
						peopleNum:200,
					},
				]
			}
		},
		methods: {
			
		},
		components:{Banner,ActivityItem},
	}
</script>

<style scoped>
	.wholeContainer{
		background-color: lightgray;
	}
	.activityItemContainer{
		background-color: lightgray;
	}
	.activityItemContainer ActivityItem{
		margin: 20rpx 0;
	}
</style>
