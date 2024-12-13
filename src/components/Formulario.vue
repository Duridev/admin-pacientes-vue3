<script setup>
import { ref } from 'vue'

const nombre = ref('Max')

const leerNombre = e => {
    nombre.value = e.target.value
}

</script>


<template>
    <div class="md:w-1/2">
        <h2 class="font-black text-3xl text-center">Seguimiento de Pacientes</h2>

        <p class="text-lg mt-5 text-center scroll-mb-8">
            Añade Pacientes y 
            <span class="text-indigo-600 font-bold">Adminístralos</span>
        </p>

        <form
        class="bg-white shadow-md rounded-lg py-10 px-5 my-10"
        >
            {{ nombre }}
            <div class="mb-5 ">
                <label 
                    for="mascota"
                    class="block text-gray-700 uppercase font-bold"
                >
                    Nombre mascota
                </label>
                <input 
                    id="mascota"
                    type="text"
                    placeholder="Nombre de la mascota"
                    class="w-full px-3 py-2 mt-1 text-gray-700 bg-gray-50 rounded-md focus:outline-none focus:shadow-outline focus:border-gray-400 border-2 border-gray-200"
                    v-on:input="leerNombre"
                    :value="nombre"
                >
            </div>

            <div class="mb-5 ">
                <label 
                    for="dueno"
                    class="block text-gray-700 uppercase font-bold"
                >
                    Nombre Dueño de la mascota
                </label>
                <input 
                    id="dueno"
                    type="text"
                    placeholder="Dueño de la mascota"
                    class="w-full px-3 py-2 mt-1 text-gray-700 bg-gray-50 rounded-md focus:outline-none focus:shadow-outline focus:border-gray-400 border-2 border-gray-200"
                >
            </div>

            <div class="mb-5 ">
                <label 
                    for="email"
                    class="block text-gray-700 uppercase font-bold"
                >
                    Email
                </label>
                <input 
                    id="email"
                    type="text"
                    placeholder="Email del dueño"
                    class="w-full px-3 py-2 mt-1 text-gray-700 bg-gray-50 rounded-md focus:outline-none focus:shadow-outline focus:border-gray-400 border-2 border-gray-200"
                >
            </div>

            <div class="mb-5 ">
                <label 
                    for="alta"
                    class="block text-gray-700 uppercase font-bold"
                >
                    Alta
                </label>
                <input 
                    id="alta"
                    type="date"
                    class="w-full px-3 py-2 mt-1 text-gray-700 bg-gray-50 rounded-md focus:outline-none focus:shadow-outline focus:border-gray-400 border-2 border-gray-200"
                >
            </div>

            <div class="mb-5 ">
                <label 
                    for="sintomas"
                    class="block text-gray-700 uppercase font-bold"
                >
                    Síntomas
                </label>
                <textarea 
                    id="sintomas"
                    type="text"
                    placeholder="Describe los síntomas"
                    class="w-full px-3 py-2 mt-1 text-gray-700 bg-gray-50 rounded-md focus:outline-none focus:shadow-outline focus:border-gray-400 border-2 border-gray-200 h-40"
                />
            </div>
            
            <input type="submit" class="bg-indigo-600 text-white p-3 uppercase rounded-md mt-5 w-full hover:bg-indigo-700 cursor-pointer transition-colors font-bold" value="Registrar Paciente">
        </form>
    </div>
</template>

