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