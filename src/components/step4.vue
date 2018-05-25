<template name="step_3">
	<v-container fluid fill-height justify-center class="bgMain st2">
		<transition   
			name="custom-classes-transition"
			enter-active-class="animated tada"
			leave-active-class="animated bounceOutRight"
		>
		<v-flex  xs12 sm6>
			<v-card flat>
				
				<v-card-media transition="scale-transition">

				<img src="https://privateflows.com/lp/game/2/confirm_age.png" alt="" height="250px">
				</v-card-media>
			
				<transition enter-active-class="animated tada" leave-active-class="animated bounceOutRight">
					<v-card-actions>
						<div class="prev" large flat @click="changeStep(nextStep)" ><img src="https://privateflows.com/lp/game/2/age.png" onmouseover="this.src='https://privateflows.com/lp/game/2/age_over.png'" onmouseout="this.src='https://privateflows.com/lp/game/2/age.png'" alt="" height="100px"> </div>
					</v-card-actions>
				</transition>
			</v-card>
		</v-flex>
		</transition>
	</v-container>
</template>

<script>
//import button1 from "./buttons/button1.vue"
	export default {
		props: {
			current:{
				type: Number,
				default: 3
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
.bgMain.st2{
	background-image: url("https://privateflows.com/lp/game/2/bg-5.jpg");
	background-size: cover;
}
</style>


