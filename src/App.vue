<template>
	<v-app dark>
		 <v-flex fill-height fluid>
			 <transition   name="custom-classes-transition"
    leave-active-class="animated bounceOutRight">
				<step
					@changeStep="toStep"
					:is="currentStep"
				></step>
			</transition>
		</v-flex>
	</v-app>
</template>

<script>
	import step1 from "./components/step1.vue"
	import step2 from "./components/step2.vue"
	export default {
		components: {
			step1, 
			step2
		},
		data() {
			return {
				currentStep: 'step1'
			}
		},
		methods:{
			toStep: function (step) {
				this.currentStep = step
			}
		}
	}
</script>

<style>
/* 	.bgMain{
		min-height: 100vh
	} */
.bgMain .card{
	display: flex;
	justify-content:center;
	align-items: flex-end;
	min-height:50%;
	width: 50%
	}
.fade-enter-active, .fade-leave-active {
  transition: opacity .5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active до версии 2.1.8 */ {
  opacity: 0;
}
</style>
