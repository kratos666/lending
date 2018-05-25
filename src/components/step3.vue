<template name="step_3">
	<v-container fluid fill-height justify-center class="bgMain st2">
		<transition   
			name="custom-classes-transition"
			enter-active-class="animated tada"
			leave-active-class="animated bounceOutRight"
		>
		<v-flex  xs12 sm6 align-center>
			<v-card flat>
				<transition enter-active-class="animated tada" leave-active-class="animated bounceOutRight">
					<v-card-actions>
						<v-btn top class="prev" large flat @click="changeStep(nextStep)"><img src="https://privateflows.com/lp/game/2/btn-small.png" alt="" height="60px"> </v-btn>
						<v-btn top class="next" large flat @click="changeStep(nextStep)"><img src="https://privateflows.com/lp/game/2/btn-medium.png" alt="" height="60px"> </v-btn>
					</v-card-actions>
				</transition>

				<v-card-media>

				<img src="https://privateflows.com/lp/game/2/dick.png" alt="">
				</v-card-media>
	
				<transition enter-active-class="animated tada" leave-active-class="animated bounceOutRight">
					<v-card-actions>
						<v-btn class="prev" large flat @click="changeStep(nextStep)"><img src="https://privateflows.com/lp/game/2/btn-large.png" alt="" height="60px"> </v-btn>
						<v-btn class="next" large flat @click="changeStep(nextStep)"><img src="https://privateflows.com/lp/game/2/btn-massive.png" alt="" height="60px"> </v-btn>
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
	background-image: url("https://privateflows.com/lp/game/2/bg-3.jpg");
	background-size: cover;
}
</style>


