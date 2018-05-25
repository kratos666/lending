<template name="step_1">
	<v-container fill-height fluid justify-center class="bgMain st1">
	
		<transition name="custom-classes-transition" enter-active-class="animated tada" leave-active-class="animated bounceOutRight">
		<v-flex  xs12 sm6 >
			<v-card flat>

				<v-card-media>
				<img src="https://privateflows.com/lp/game/2/gender.png" alt="">
				</v-card-media>
	
				<transition enter-active-class="animated tada" leave-active-class="animated bounceOutRight">
					<v-card-actions>
						<v-btn class="prev" large flat @click="changeStep(prevStep)"><img src="https://privateflows.com/lp/game/2/male.png" alt="" height="60px"> </v-btn>
						<v-btn class="next" large flat @click="changeStep(nextStep)"><img src="https://privateflows.com/lp/game/2/female.png" alt="" height="60px"> </v-btn>
					</v-card-actions>
				</transition>
			</v-card>
			</v-flex>
		</transition>
	</v-container>
</template>

<script>
	//import button1 from "./buttons/button1.vue";
	
	export default {
		props: {
			current:{
				type: Number,
				default: 1
			}
		},
		computed:{
			nextStep: function () {
				return this.current + 1
			},
			prevStep: function () {
				return this.current - 1
			}
		},
		methods: {
			changeStep: function(step){
				this.$emit('step-change', step)
			}
		}
	}
</script>

<style scoped>
	.bgMain.st1 {
		background-image: url("https://privateflows.com/lp/game/2/bg-1.jpg");
	}
	
	.slide-fade-enter-active {
		transition: all 0.3s ease;
	}
	.slide-fade-leave-active {
		transition: all 0.8s cubic-bezier(1, 0.5, 0.8, 1);
	}
	.slide-fade-enter,
	.slide-fade-leave-to
	/* .slide-fade-leave-active до версии 2.1.8 */
	{
		transform: translateX(10px);
		opacity: 0;
	}
</style>


