<script setup>
import { ref } from 'vue'

let peticion1 = {
    libro1: "hola",
    usuario: "juan",
    estado: "aprobado"
}
let peticion2 = {
    libro1: "gsg",
    usuario: "jorge",
    estado: "rechazado"
}
let peticion3 = {
    libro1: "wtgt",
    usuario: "carlos",
    estado: "en espera"
}

let peticiones = ref([
    peticion1, peticion2, peticion3
])

</script>

<template>
    <div class="margen">

        <div v-for="peticion in peticiones" class="card" style="width: 30rem;">
            <div class="card-body">
                <div class="container-carta">
                    <h5 class="card-title"><b>Solicitaste el libro: </b> {{ peticion.libro1 }}</h5>
                    <h5 class="card-title"><b>Al usuario: </b> {{ peticion.usuario }}</h5>
                    <h5 class="card-title"><b>Estado de la solicitud: </b> {{ peticion.estado }}</h5>
                </div>
            </div>

        </div>

    </div>
</template>

<!--
    tiene que haber un botón que si la peticion no esta en espera (aceptado o rechazado) aparece.
    con ese botón eliminas la petición. popeas del array la petición
-->

<style scoped>
.margen {
    margin: 20px 0px 0px 20px;
}
</style>