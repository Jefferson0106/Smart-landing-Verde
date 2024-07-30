<script>
import axios from 'axios';
import { toast } from 'vue3-toastify';
import 'vue3-toastify/dist/index.css';

export default {
  name: "NuevoQsd",
  data: function() {
    return {
      ID: null,
      form: {
        id: "",
        nombre: "",
        correo: "",
        telefono: "",
        nombreEmpresa: "",
        mensaje: "",
        Token: "",
      }
    };
  },
  methods: {
    registrar() {
      this.form.Token = localStorage.getItem("Token");
      axios.post("https://smartsalesagent-api.azurewebsites.net/SmartBotForWhatsApp/Registro", this.form)
        .then(data => {
          console.log(data);
          // Mostrar notificación de éxito
          toast.success("¡Registro creado con éxito!", {
            autoClose: 3000,
          });
          this.$router.push("/");
        })
        .catch(error => {
          console.error(error);
          // Mostrar notificación de error
          toast.error("Hubo un error al crear el registro.", {
            autoClose: 3000,
          });
        });
    },
  }
};
</script>

<template>
	<div>
	  <div class="contenedor">
		<h1 class="titulo">¿Cómo Funciona?</h1>
		<p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Voluptatum, m?</p>
		<p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Voluptatum, m?</p>
		  <img class="imagen" src="/assets/img/pixele.png" alt="">
		  <div class="project-bg">
			<img class="video" src="/assets/img/video2.png" alt="">

			<h1 class="clase">Testimonios</h1>
			<p class="texto54">Lorem ipsum dolor sit amet consectetur adipisicing elit. Sim</p>
			<p class="texto54">fh eie odja Lorem ipsum dolor sit amet consectetur  </p>
			<h6 class="hola">John Doe</h6>

			<img class="persona" src="/assets/img/persona.png" alt="">

			<img class="persona" src="/assets/img/persona.png" alt="">

			<img class="persona" src="/assets/img/persona.png" alt="">


			<!-----Login-->

			<h2 class="title">¡Regístrate ahora y dale un nuevo enfoque a tu negocio!</h2>
			<form class="form-overlay">
    <div class="kimber">
      <input type="text" id="name" name="name" placeholder="Nombre completo" v-model="form.nombre">
      <input type="email" id="email" name="email" placeholder="Correo electrónico" v-model="form.correo">
      <input type="text" id="phone" name="phone" placeholder="Teléfono" v-model="form.telefono">
      <input type="text" id="company" name="company" placeholder="Empresa" v-model="form.nombreEmpresa">
      <textarea id="message" name="message" placeholder="Mensaje [opcional]" v-model="form.mensaje"></textarea>
      <button type="button" class="azul" @click="registrar">Comienza Ahora</button>
    </div>
  </form>

			<!-----Login-->
			<div>
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
			
			
	  </div>
	  </div>
	  </div>
	</template>
	
	<style scoped>


@media (max-width: 767px) {
	.contenedor {
		  text-align: center;
		  /* Personaliza otros estilos aquí */
	  }
	  .titulo{
		color: beige;
		font-size: 40px;
		top: 40px;
		left: -20px;
	  }
	  p{
		margin:  -40px;
		color: beige;
		font-size: 10px;
		top: 120px;
		left: -20px;
	  }
	  .imagen{
		  top: 950px;
		left: -20px;
	  }
.clase{
	top: -90px;
		left: -53px;
		font-size: 40px;
		margin: 140px;
		color: #FFFFFF;

		
}
.persona{
	width: 10%;
	padding: 8px;
	margin: 30px;
}
.texto54{
	width: 100%;
	top: -140px;
	left: 30px;
	padding: -70;
	color: #FFFFFF;
}
.video{
	top: -500px;
	left: -100px;
	padding: 40px;
	margin: 10px;
}
.hola{
	color: #FFFFFF;
	top: -10px;
	left: -20px;
}


}

@media (min-width: 768px) {
	.contenedor {
		  text-align: center;
		  /* Personaliza otros estilos aquí */
	  }
	  .titulo{
		color: beige;
		font-size: 40px;
		top: 140px;
		left: -50px;
	  }
	  p{
		margin:  -60px;
		color: beige;
		top: 240px;
		left: -20px;
	  }
	  .imagen{
		  top: 950px;
		left: -20px;
	  }
.clase{
	top: -150px;
		left: -530px;
		font-size: 40px;
		margin: 140px;
		color: #FFFFFF;

		
}
.persona{
	width: 10%;
	padding: 8px;
	margin: 30px;
}
.texto54{
	width: 100%;
	top: -140px;
	left: 30px;
	padding: -70;
	color: #FFFFFF;
}
.video{
	top: -500px;
	left: -100px;
	padding: 40px;
	margin: 10px;
}
.hola{
	color: #FFFFFF;
	top: -10px;
	left: -20px;
}



}
	 




/* registro del login */

@media (max-width: 767px) {


	.form-overlay {
		position: absolute;
            top: 960%;
            left: 50%;
            transform: translate(-50%, -50%);
        background-color: #FFFFFF; /* Fondo semitransparente */
            padding: 10px;
            border-radius: 1px;
            width: 80%; /* Ajusta el ancho según sea necesario */
            box-shadow: 0 4px 8px black;
    }
	input[type="text"], select, textarea {
    width: 100%;
    padding: 12px;
    border: 1px solid #ccc;
    border-radius: 4px;
    box-sizing: border-box;
    resize: vertical;
}

/* Estilo para las etiquetas que se muestran junto a los campos */
label {
    padding: 12px 12px 12px 0;
    display: inline-block;
}

/* Estilo para el botón de envío */
input[type="submit"] {
    background-color: #04AA6D;
    color: white;
    padding: 12px 20px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    float: right;
}

/* Estilo para el contenedor del formulario */
.container {
    border-radius: 5px;
    background-color: #f2f2f2;
    padding: 20px;
}

/* Columna flotante para las etiquetas: ancho del 25% */
.col-25 {
    float: left;
    width: 25%;
    margin-top: 6px;
}

/* Columna flotante para los campos de entrada: ancho del 75% */
.col-75 {
    float: left;
    width: 75%;
    margin-top: 6px;
}

/* Limpieza de flotantes después de las columnas */
.row:after {
    content: "";
    display: table;
    clear: both;
}
.azul{
		 width: 30%;
		   padding: 10px;
		   top: 10px;
		   background-color: #FFFFFF ;
		   color: black;
		   border: 1px solid #66CDAA;
		   border-radius: 5px;
		   cursor: pointer;
		   margin: 0 auto; 
 display: block;
}

.title {
		  
	text-align: center;
            top: 30px;
            left: 3%;
			font-size: 15px;
            color: #FFFFFF; 
            background-color: transparent;
            padding: 5px;
            border-radius: 5px;
            white-space: nowrap; 
		   
		  
	   }








.robo3{
	width: 20%;
	position: relative;
            left: 10px; 
            top: 660px;  
			margin: 20px;
        }
.faq{
	position: relative;
            left: -140px; 
            top: 700px;  
			margin: 20px;
			color: #f2f2f2;
}
.faque{
	position: relative;
            left: -50px; 
            top: 660px;  
			font-size: 10px;
			margin: 50px;
			color: #FFFFFF;
}
.mensaje3{
	width: 30%;
	position: relative;
            left: 20px; /* Ajusta este valor para mover la imagen horizontalmente */
            top: 100px;  /* Ajusta este valor para mover la imagen verticalmente */
			margin: 50px;
			
}
.mensaje4{
	width: 30%;
	position: relative;
            left: 330px; /* Ajusta este valor para mover la imagen horizontalmente */
            top: 300px;  /* Ajusta este valor para mover la imagen verticalmente */
			margin: 50px;
			font-size: 1px;
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
			left: 100px; /* Ajusta este valor para mover la imagen horizontalmente */
            top: 450px;  /* Ajusta este valor para mover la imagen verticalmente */
			
            color: black;
        }
.texto1{
	position: relative;
			left: 100px; 
            top: 240px; 
            color: black;
}
.texto2{
	position: relative;
			left: 100px; 
            top: 30px; 
            color: black;
}
.texto3{
	position: relative;
			left: 100px; 
            top: -180px; 
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
}



@media (min-width: 768px) {


.form-overlay {
		 position: relative;
		   top: 240px;
		   left: 640px;
		   margin: 60px;
		   transform: translate(-50%, -50%);
		   background-color: #FFFFFF;
		   padding: 20px;
		   border-radius: 10px;
		   width: 80%; 
		   box-shadow: 0 4px 8px black;
	   }

	   .form-overlay h2 {
		   text-align: center;
		   color: #007BFF;
	   }

	   .form-overlay label {
		   display: block;
		   margin-bottom: 5px;
		   color: black;
	   }

	   .form-overlay input[type="text"],
	   .form-overlay input[type="email"],
	   .form-overlay textarea {
		   width: 100%;
		   padding: 10px;
		   margin-bottom: 10px;
		   border: 1px solid #ccc;
		   border-radius: 5px;
		   color: black; 
	   }
.azul{
		 width: 30%;
		   padding: 10px;
		   top: 10px;
		   background-color: #FFFFFF ;
		   color: black;
		   border: 1px solid #66CDAA;
		   border-radius: 5px;
		   cursor: pointer;
		   margin: 0 auto; 
 display: block;
}

.title {
		  
		   top: -10px;
		   left: 650px;
		   margin: 40px;
		   transform: translateX(-50%);
		   color: #FFFFFF; 
		   background-color: transparent;
		   padding: 5px;
		   border-radius: 5px;
		   white-space: nowrap; 
	   }








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
            top: -450px;  /* Ajusta este valor para mover la imagen verticalmente */
            color: black;
        }
.texto1{
	position: relative;
			left: 400px; 
            top: -840px; 
            color: black;
}
.texto2{
	position: relative;
			left: 400px; 
            top: -1240px; 
            color: black;
}
.texto3{
	position: relative;
			left: 400px; 
            top: -1630px; 
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
	}
	</style>
  <!---padding: 40px;
	margin: 100px;-->