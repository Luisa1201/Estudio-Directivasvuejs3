<script setup>
import{ref, computed} from 'vue'
const num = "Hola mundo"
const arrayUsuarios =[
  {
    nombre: 'Marta',
    grado: 'Tercero',
    edad: '10'
  },
  {
    nombre: 'Carlos',
    grado: 'Tercero',
    edad: '13'
  },
  {
    nombre: 'Laura',
    grado: 'Tercero'
  }

];

const nume = ref(0)

nume.value = 2

const computado = computed(function (){ 
  return nume.value > 0 ? nume.value * 2 : 0
})

</script>

<template>
  <h1>{{ num }}</h1> <br>
  valor completado {{  computado }} <br>

  <div v-for="(usuario,index) in arrayUsuarios" :key="index">
    Nombre: {{ usuario.nombre }} <br>
    Grado: {{ usuario.grado }} <br>
    <span v-if="usuario.edad">
      Edad: {{ usuario.edad }}
    </span>
    

  </div>



  
</template>

<style scoped>

h1{
  color:blue;
}

</style>
