<template>
	<v-app dark>
		 <v-flex fill-height fluid>
			 <transition   name="custom-classes-transition"
    leave-active-class="animated bounceOutRight">
				<step
					:current="step"
					@step-change="toStep"
					:is="curStep"
				></step>
			</transition>
		</v-flex>
	</v-app>
</template>

<script>
	import step_1 from "./components/step1.vue"
	import step_2 from "./components/step2.vue"
	import step_3 from "./components/step3.vue"
	import step_4 from "./components/step4.vue"
	export default {
		components: {
			step_1, 
			step_2,
			step_3,
			step_4
		},
		data() {
			return {
				curStep: 'step_1',
				step: 1
			}
		},
		methods:{
			toStep: function (step) {
				var str = this.curStep;
				this.curStep = str.slice(0, -1)  + step;
				this.step = step;
			}
		}
	}
</script>

<style>
.bgMain{
	background-position: center;
	background-size: cover;
	} 
.bgMain .card{
	background-color: transparent;
	}

.bgMain .card .card__actions{
	justify-content: space-around;
}
.fade-enter-active, .fade-leave-active {
  transition: opacity .5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active до версии 2.1.8 */ {
  opacity: 0;
}
</style>
