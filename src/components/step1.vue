<template name="step1">
	<v-container fill-height fluid justify-center class="bgMain st1">
		<transition   name="custom-classes-transition"
    enter-active-class="animated tada"
    leave-active-class="animated bounceOutRight">
			<v-card >
				<transition>
					<button1></button1>
				</transition>
			</v-card>
		</transition>
	</v-container>
</template>

<script>
	import button1 from "./buttons/button1.vue"
	export default {
		components:{
			button1
		},
		data() {
			return{

			}
		}
	}
</script>

<style scoped>

.bgMain.st1{
	background-image: url("https://u01.appmifile.com/images/2017/04/15/c9b37bf4-2bed-466f-b2a1-e3bee2e54d7c.jpg");
	background-size: cover;
}
.st1 .card{
	background-image: url("https://u01.appmifile.com/images/2017/04/15/7aaad7ae-81b2-4066-8f89-7abc9b8ffb2e.jpg");
	background-size: contain
}

.slide-fade-enter-active {
  transition: all .3s ease;
}
.slide-fade-leave-active {
  transition: all .8s cubic-bezier(1.0, 0.5, 0.8, 1.0);
}
.slide-fade-enter, .slide-fade-leave-to
/* .slide-fade-leave-active до версии 2.1.8 */ {
  transform: translateX(10px);
  opacity: 0;
}

</style>


