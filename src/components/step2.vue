<template name="step_2">
	<v-container fluid fill-height justify-center class="bgMain st2">
		<transition   
			name="custom-classes-transition"
			enter-active-class="animated tada"
			leave-active-class="animated bounceOutRight"
		>
		<v-flex  xs12 sm6 align-center  justify-center>
			<v-card flat>
				<v-card-media>
				<img src="https://privateflows.com/lp/game/2/character.png" alt="">
				</v-card-media>
	
				<transition name="fade">
					<v-card-actions>
						<v-btn class="prev" large flat @click="changeStep(prevStep)"><img src="https://privateflows.com/lp/game/2/female1.png" alt="" height="60px"> </v-btn>
						<v-btn class="next" large flat @click="changeStep(nextStep)"><img src="https://privateflows.com/lp/game/2/female2.png" alt="" height="60px"> </v-btn>
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
				default: 2
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
	background-image: url("https://privateflows.com/lp/game/2/bg-2.jpg");
	background-size: cover;
}

   .fade-enter-active, .fade-leave-active {
            transition: opacity 5s
         }
	.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
		opacity: 0
	}
</style>


