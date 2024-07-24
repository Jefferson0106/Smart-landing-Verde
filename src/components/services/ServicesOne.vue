<script setup>

import { onMounted, ref, onUpdated } from 'vue'

import axios from "axios";

const services = ref([]);

onMounted(async () => {
  const { data: fetchedServices } = await axios.get("/data/services.json");
  services.value = fetchedServices.services;
});

onUpdated(() => {     

		// Service Slider    
        $(".service-slider").owlCarousel({
		loop: true,
		items: 3,
		dots: true,
		nav: false,
		smartSpeed: 1000,
		autoHeight: false,
		touchDrag: true,
		mouseDrag: true,
		margin: 30,
		autoplay: true,
		slideSpeed: 600,
		responsive: {
			0: {
				items: 1,
				nav: false,
				dots: false,
			},
			600: {
				items: 2,
				nav: false,
				dots: false,
			},
			768: {
				items: 2,
				nav: false,
				dots: false,
			},
			1100: {
				items: 3,
				nav: false,
				dots: true,
			}
		}
	});
  
});

</script>

<template>
	<div class="hero-area-bg-2">
    <div class="feature-area section-padding">
 		<div class="container">
 			<div class="row">
 				<div class="col-lg-6 col-md-12 col-sm-12">
 					<div class="section-title">
 						<!---h6>Features</h6> --->
 						<h2 class="computadora"><span class="punto"></span>Integracion Sencilla Con <b></b></h2>
						 <h2 class="computadora"><b>Sistema Existente</b></h2>
						 <p class="textoparrafo"> Lorem ipsum dolor sit amet consectetur adipisicing elit. Nisi libero placeat nemo iusto quaerat sequi veritatis aliquam accusamus tempore ratione error, assumenda ullam! Cumque at eveniet accusantium maxime enim quos.</p>
 					</div>
					
 					<!--div 
					>
 						<div class="feature-icon">
 							<i :class="feature.icon"></i>
 						</div> ---->
 						<!---div class="feature-content">
 							<h5>{{ feature.title }}</h5>
 							<p>{{ feature.content }}</p>
 						</div> 
 					</div> 	--->			
 				</div>
				
 				<div class="col-lg-6 col-md-12 col-sm-12">
 					<div class="feature-image">
 						<img src="/assets/img/computer.png" alt="">
 					</div>
 				</div>
 			</div>
 		</div>
 	</div>
	</div>
</template>


<style scoped>
.computadora{
	top: 100px;
	left: 1px;
	font-size: 40px;
	color: #2E8B57;
	
}
.punto {
	width: 30px;
	height: 20px;
	background-color: #2E8B57;
	border-radius: 50%;
	margin-right: 10px;
	
} 
.textoparrafo{
	top: 100px;
	left: 20px;
}
</style>












<!----div class="services-area gray-bg section-padding pad-bot-90">
	<div class="container">
		<div class="row">
			<div class="offset-lg-2 col-lg-8 text-center">
				<div class="section-title">
					<h6>Services</h6>
					<h2>Providing the Best Global <b>Industry Services</b></h2>
				</div>
			</div>
		</div>

		<div class="row mt-30">
			<div class="col-lg-12">
				<div class="service-slider owl-carousel">
					<div class="single-service-area"
				   v-for="service in services.slice(0,6)" :key="service.id"
				   >
						<div class="service-icon">
							<i :class="service.icon"></i>
						</div>
						<h5>{{ service.title }}</h5>
						<p>{{ service.content }}</p>
						<router-link :to="{name:'service-details'}" class="read-more">Read More</router-link>
					</div> 						
				</div>
			</div>
		</div>
	</div>
</div> --->