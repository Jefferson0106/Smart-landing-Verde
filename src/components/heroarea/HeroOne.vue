<script setup>

import { onMounted } from 'vue'

onMounted(() => {     

	$('.homepage-slides').owlCarousel({
		items: 1,
		dots: false,
		nav: true,
		loop: true,
		autoplay: true,
		autoplayTimeout: 5000,
		smartSpeed: 2000,
		slideSpeed: 600,
		animateOut: 'fadeOut',
		navText: ["<i class='la la-angle-left'></i>", "<i class='la la-angle-right'></i>"],
		responsive: {
			0: {
				items: 1,
				nav: false,
				dots: false,
			},
			600: {
				items: 1,
				nav: false,
				dots: false,
			},
			768: {
				items: 1,
				nav: false,
				dots: false,
			},
			1100: {
				items: 1,
				nav: true,
				dots: false,
			}
		}
	});


	$(".homepage-slides").on("translate.owl.carousel", function () {
		$(".single-slide-item h1").removeClass("animated fadeInUp").css("opacity", "1");
		$(".single-slide-item h6").removeClass("animated fadeInDown").css("opacity", "1");
		$(".single-slide-item p").removeClass("animated fadeInDown").css("opacity", "1");
		$(".single-slide-item a.main-btn").removeClass("animated fadeInDown").css("opacity", "1");
	});

	$(".homepage-slides").on("translated.owl.carousel", function () {
		$(".single-slide-item h1").addClass("animated fadeInUp").css("opacity", "1");
		$(".single-slide-item h6").addClass("animated fadeInDown").css("opacity", "1");
		$(".single-slide-item p").addClass("animated fadeInDown").css("opacity", "1");
		$(".single-slide-item a.main-btn").addClass("animated fadeInDown").css("opacity", "1");
	});
  
});

</script>

<template>
    <div> <!---class="homepage-slides owl-carousel"--->
 		<div class="single-slide-item">
 			<!--div class="overlay"></div> --->
 			<div class="hero-area-content">
 				<div class="container">
 					<div class="row justify-content-center">
 						<div class="col-lg-12 wow fadeInUp animated" data-wow-delay=".2s">
 							<div class="section-title">
								<img class="imagenrobo" src="/assets/img/robo.png" alt="">
 								<!--h6 class="text-white">AUTOMATIZA, OPTIMIZA Y MEJORA</h6> -->
								
 								<h1 class="letraverde">AUTOMATIZA, OPTIMIZA Y MEJORA<br>LA EXPERIENCIA DEL CLIENTE</h1>
 								<p class="textop"> Industrial Revolution, in modern history, the process of change from an agrarian <br>and handicraft economy to one dominated by industry and machine manufacturing.</p>
 							</div>
 							<router-link :to="{name:'about'}" class="main-btn">Learn More</router-link>
 						</div>
 					</div>
 				</div>
 			</div>
 		</div>

 		<!--div class="single-slide-item hero-area-bg-2">
 			<div class="overlay"></div>
 			<div class="hero-area-content">
 				<div class="container">
 					<div class="row justify-content-center">
 						<div class="col-lg-12 wow fadeInUp animated" data-wow-delay=".2s">
 							<div class="section-title">
 								<h6 class="text-white">We provide best satisfied work</h6>
 								<h1>We turn vision<br> Factory Solutions</h1>
 								<p> Industrial Revolution, in modern history, the process of change from an agrarian <br>and handicraft economy to one dominated by industry and machine manufacturing.</p>
 							</div>
 							<router-link :to="{name:'about'}" class="main-btn">Learn More</router-link>
 						</div>
 					</div>
 				</div>
 			</div> 
 		</div> --->
 	</div>
</template>

<style scoped>
.letraverde{
	top: 0px;
	left: 10px;
	font-size: 40px;
	color: #2E8B57;
	text-align: left;
}
.imagenrobo{
	width: 40%;
	float: right;
	margin-left: 20px;
}
.textop{
	top: 0px;
	left: 10px;
	color: #000;
}
</style>