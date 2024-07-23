<template>
    <footer class="footer-area">
 		<div class="container">
 			<div class="footer-up">
 				<div class="row gy-5">
 					<div class="col-lg-3 col-md-6 col-sm-12">
 						<div class="logo">
 							<img class="imagen" src="/assets/img/logo1.png" alt="dustrian-logo">
 						</div>
 					</div>
 					<div class="col-lg-2 offset-lg-1 col-md-6 com-sm-12">
 						<h5>Dolorlsit</h5>
 						<ul>
 							<li>
 								<router-link :to="{name:'about'}">Lorem ipsum</router-link>
 								<router-link :to="{name:'project'}">Ipsum</router-link>
 								<router-link to="/">Amet</router-link>
 							</li>
 						</ul>
 					</div>
 					<div class="col-lg-3 col-md-6 col-sm-12">
 						<h5>Legal</h5>
 						<ul>
 							<li>
 								<router-link :to="{name:'service-details'}"><span>-</span>Politica De Privacidad</router-link>
 								<router-link :to="{name:'service-details'}"><span>-</span> Terminos De uso</router-link>
 							</li>
 						</ul>
 					</div>
 					<div class="col-lg-3 col-md-6">
 						<div class="subscribe-form">
 							<!--h5>Newsletter</h5>
 							<p>Sign Up now for latest news update</p> -->
 							<form>
								<div class="social-area">
 							<a href=""><i class="lab la-facebook-f"></i></a>
 							<a href=""><i class="lab la-instagram"></i></a>
 							<a href=""><i class="lab la-twitter"></i></a>
 							<a href=""><i class="la la-skype"></i></a>
 						</div>
 							</form>
 						</div>
 					</div>
 				</div>
 			</div>
 		</div>
 	</footer>
</template>

<style scoped>
.imagen{
	top: 100px;
	left: 100px;
}
</style>