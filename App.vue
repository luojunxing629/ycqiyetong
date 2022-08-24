<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
			 uni.onTabBarMidButtonTap(function(e){
			                uni.navigateTo({
			                    url: '../add/add',
			                    animationType: "slide-in-bottom", // 动画类型
			                    animationDuration: 150, // 窗口动画持续时间，单位为 ms
			                    fail(err) {
			                        console.log(err)
			                    }
			                })
			            })
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style lang="scss">
	/*每个页面公共css */
	@import "@/uni_modules/uview-ui/index.scss";
</style>
