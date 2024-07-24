<script setup>

import { onMounted, onUpdated, ref } from "vue";
import axios from "axios";

const testimonials = ref([]);

onMounted(async () => {
  const { data: fetchedTestimonials } = await axios.get("/data/testimonials.json");
  testimonials.value = fetchedTestimonials.testimonials;
});

onUpdated(() => {     

    $('.testimonial-carousel').owlCarousel({
		items: 1,
		margin: 30,
		dots: true,
		nav: false,
		loop: true,
		autoplay: true,
		responsiveClass: true,
		responsive: {
			575: {
				items: 1,
				nav: false,
				dots: false,
			},

			767: {
				items: 2,
				nav: false
			},

			990: {
				items: 2,
				loop: true,

			},
			1200: {
				items: 3,
				dots: true,
				loop: true,
			}
		}
	});

  
});

</script>


<template>
<div class="project-bg">
				<h1 class="faq">FAQ</h1>
				<p class="faque">Lorem ipsum dolor sit amet consectetur,atior gdr erys sikkza </p>

					<img class="robo3" src="/assets/img/robo1.png" alt="">
					<img class="mensaje3" src="/assets/img/mensaje.png" alt="">
					<h6 class="texto">Lorem ipsum dolor sit amet</h6>
					<span class="signo">^</span>

					<img class="mensaje4" src="/assets/img/mensaje.png" alt="">
					<h6 class="texto1">Lorem ipsum dolor sit amet</h6>
					<span class="signo">^</span>

					<img class="mensaje5" src="/assets/img/mensaje.png" alt="">
					<h6 class="texto2">Lorem ipsum dolor sit amet</h6>
					<span class="signo">^</span>

					<img class="mensaje6" src="/assets/img/mensaje.png" alt="">
					<h6 class="texto3">Lorem ipsum dolor sit amet</h6>
					<span class="signo">^</span>

					<!---img class="mensaje7" src="/assets/img/mensaje.png" alt="">
					<h6 class="texto4">Lorem ipsum dolor sit amet</h6>
					<span class="signo">^</span> --->

			</div>
 
</template>

<style scoped>

.robo3{
	width: 20%;
	position: relative;
            left: 10px; 
            top: 200px;  
			margin: 20px;
        }
.faq{
	position: relative;
            left: -510px; 
            top: 200px;  
			margin: 20px;
			color: #FFFFFF;
}
.faque{
	position: relative;
            left: -350px; 
            top: 200px;  
			margin: 50px;
			color: #FFFFFF;
}
.mensaje3{
	width: 30%;
	position: relative;
            left: 260px; /* Ajusta este valor para mover la imagen horizontalmente */
            top: -100px;  /* Ajusta este valor para mover la imagen verticalmente */
			margin: 50px;
}
.mensaje4{
	width: 30%;
	position: relative;
            left: 430px; /* Ajusta este valor para mover la imagen horizontalmente */
            top: -500px;  /* Ajusta este valor para mover la imagen verticalmente */
			margin: 50px;
}
.mensaje5{
	width: 30%;
	position: relative;
            left: 430px; /* Ajusta este valor para mover la imagen horizontalmente */
            top: -900px;  /* Ajusta este valor para mover la imagen verticalmente */
			margin: 50px;
}.mensaje6{
	width: 30%;
	position: relative;
            left: 430px; /* Ajusta este valor para mover la imagen horizontalmente */
            top: -1290px;  /* Ajusta este valor para mover la imagen verticalmente */
			margin: 50px;
}
.mensaje7{
	width: 30%;
	position: relative;
            left: 430px; /* Ajusta este valor para mover la imagen horizontalmente */
            top: -190px;  /* Ajusta este valor para mover la imagen verticalmente */
			margin: 50px;
}
.texto {
            position: relative;
			left: 400px; /* Ajusta este valor para mover la imagen horizontalmente */
            top: -420px;  /* Ajusta este valor para mover la imagen verticalmente */
            color: black;
        }
.texto1{
	position: relative;
			left: 400px; 
            top: -810px; 
            color: black;
}
.texto2{
	position: relative;
			left: 400px; 
            top: -1210px; 
            color: black;
}
.texto3{
	position: relative;
			left: 400px; 
            top: -1600px; 
            color: black;
}
.texto4{
	position: relative;
			left: 400px; 
            top: -1999px; 
            color: brown;
}
		.signo {
            position: absolute;
            top: 50%;
            left: calc(50% + 20px); /* Ajusta esta distancia según sea necesario */
            transform: translate(-50%, -50%);
            font-size: 12px; /* Ajusta el tamaño del signo según sea necesario */
            color: blue;
        }

</style>


<!----- <div class="testimonial-area gray-bg section-padding">
 		<div class="capricorn-testimonial">
 			<div class="container">
 				<div class="row">
 					<div class="col-lg-12 text-center ">
 						<div class="section-title">
 							<h6>Testimonial</h6>
 							<h2>Happy <b> Client </b>Says <br>About Us</h2>
 						</div>
 					</div>
 				</div>

 				<div class="row">
 					<div class="col-lg-12">
 						<div class="testimonial-carousel owl-carousel">
 							<div class="single-team-item"
							v-for="t in testimonials.slice(0,3)" :key="t.id"
							>
 								<div class="testimonial-icon"><i class="las la-quote-left"></i></div>
 								<p>{{ t.content }}</p>
 								<div class="testimonial-author">
									<div class="testimonial-img">
										<img :src="t.author_img" alt="">
									</div>
									<div class="author-info">
										<h5>{{ t.author_name }}</h5><span>{{ t.author_designation}}</span>
									</div>
								</div>
 							</div> 							
 						</div>
 					</div>
 				</div>
 			</div>
 		</div>
 	</div>-->