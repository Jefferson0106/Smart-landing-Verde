<script setup>

import { onMounted, ref} from 'vue'

import axios from "axios";

const blogs = ref([]);

onMounted(async () => {
  const { data: fetchedblogs } = await axios.get("/data/blogs.json");
  blogs.value = fetchedblogs.blogs;
});

</script>
<template>
    <div class="achievement-area">
     <div class="single-slide-item">
		<h2 class="title">¡Regístrate ahora y dale un nuevo enfoque a tu negocio!</h2>
        <form class="form-overlay">
			<div class="kimber">
				<input type="text" id="name" name="name" placeholder="Nombre completo">
				<input type="email" id="email" name="email" placeholder="Correo electrónico"><br><br>
                <input type="text" id="phone" name="phone" placeholder="Teléfono"><br><br>
                <input type="text" id="company" name="company" placeholder="Empresa"><br><br>
                <textarea id="message" name="message" placeholder="Mensaje [opcional]"></textarea><br><br>
                <button type="button" class="azul">Comienza Ahora</button>
			</div>
        </form>
    </div>
    </div>
</template>

<style scoped>

.form-overlay {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background-color: #FFFFFF; /* Fondo semitransparente */
            padding: 20px;
            border-radius: 10px;
            width: 80%; /* Ajusta el ancho según sea necesario */
            box-shadow: 0 4px 8px black;
        }

        .form-overlay h2 {
            text-align: center;
            color: #007BFF; /* Color del texto del encabezado */
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
			border: 1px solid #1e90ff;
            border-radius: 5px;
            cursor: pointer;
			margin: 0 auto; 
  display: block;
}

.title {
           
            top: 1px;
            left: 60%;
            transform: translateX(-50%);
            color: #FFFFFF; 
            background-color: transparent;
            padding: 5px;
            border-radius: 5px;
            white-space: nowrap; 
        }

</style>

