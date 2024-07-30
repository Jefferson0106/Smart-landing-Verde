<script setup>

import { onMounted, ref} from 'vue'

import axios from "axios";

const features = ref([]);

onMounted(async () => {
  const { data: fetchedFeatures } = await axios.get("/data/features.json");
  features.value = fetchedFeatures.features;
});


</script>

<template> 
	<div> <!--class="hero-area-bg-2"-->
		  <!---h1>BENEFICIO DE SMARTBOT</h1> -->
	  <div class="about-area section-padding">
		   <div class="container">
			   <div class="row align-items-center">
				   <div class="col-lg-6 col-md-12 col-sm-12">
					  <div class="about-img-wrap">
					  <div class="image-one wow fadeInUp" data-wow-delay=".2s" style="visibility: visible; animation-delay: 0.2s; animation-name: fadeInUp;">
						  <img class="telefono" src="/assets/img/reloj.png" alt="">
					  </div>                        
					  <!---div class="image-two wow fadeInUp" data-wow-delay=".4s" style="visibility: visible; animation-delay: 0.4s; animation-name: fadeInUp;">
						  <img src="/assets/img/about/about-page-2.jpg" alt="">
					  </div>    --->                                         
				  </div> 					
				   </div>
				   <div class="col-lg-6 col-md-12 col-sm-12">
					   <div class="info-content-area">
						   <div> <!--- class="section-title"-->
							   <!--h6>About Us</h6>-->
							   <h2 class="verdel"><span class="punto"></span>Ahorro De tiempo y <b> Recursos</b></h2>
						   </div>
						   <p class="textoparrafo">We are build construction site lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea enim et, similique minus soluta ipsum dolor sit, amet consectetur adipisicing elit.</p>
						   <!--div class="about-list-item mt-30">
							  <p class="highlight">Since our launch in 1995, to deliver high value project.</p>
							  <p class="highlight">We always provide flexible & quality task. </p>
							  <p class="highlight">Uninque latest machinary used the industrial project.</p>
						  </div>
  
						   <div class="row founded">
							   <div class="col-lg-4 col-md-6 col-12">
								   <div class="years"><span>25</span>Year of Success</div>
							   </div>
							   <div class="col-lg-8 col-md-6 col-12">
								   <div class="text">Since we established in 1995 experience &amp; still a growing protfolio day by day!</div>
							   </div>
						   </div>
					   </div> -->
				   </div>
  
			   </div>
		   </div>
	   </div>
  </div>
  </div>
  </template>
  
  <style scoped>

@media (max-width: 767px) {
	.telefono{
	  width: 70%;
	  padding: 10px;
	  margin: 20px;
  }
  .verdel{
	  top: 1px;
	  left: 1px;
	  font-size: 29px;
	  color: #2E8B57;
	  white-space: nowrap;
  }
  .textoparrafo{
	  margin: 20px;
  }

}


@media (min-width: 768px) {

  .telefono{
	  width: 70%;
	  padding: 10px;
	  margin: 20px;
  }
  .verdel{
	  top: 1px;
	  left: 1px;
	  font-size: 35px;
	  color: #2E8B57;
	  white-space: nowrap;
  }
  .textoparrafo{
	  margin: 20px;
  }
}
  </style>
  
  
  <!--<div class="achievement-area">
		   <div class="overlay-2"></div>
		   <div class="container">
			   <div class="row">
				   <div class="col-lg-3 col-md-6 col-sm-6"
				  v-for="cn in counter.slice(0,4)" :key="cn.id"
				  >
					   <div class="single-counter-box">
						   <div class="fact-icon">
							   <i :class="cn.icon"></i>
						   </div>
						   <p class="counter-number"><span>{{ cn.number }}</span></p>
						   <h6>{{ cn.title }}</h6>
					   </div>
				   </div> 				
			   </div>
		   </div>
	   </div>-->