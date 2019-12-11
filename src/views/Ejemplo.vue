<template>
  <div>
      <p>{{variable}}</p> <!-- imprime la variable "variable" -->
      <p>{{inputText}}</p> <!-- imprime la variable "inputText" -->
      <p v-if="inputText === 'xd'">Ja, xD</p> <!-- se imprime solo si "inputText" es xd -->
      
      <input type="text" v-model="inputText"> <!-- cambia automaticamente la variable "inputText" -->

      <p v-for="(item, index) in array" :key="index">{{item}}</p> <!-- recorre el array "array" -->

      <button @click="funtion1">Exec func 1</button> <!-- ejecuta la "funtion1" -->
      <button @click="funtion2">Exec func 2</button> <!-- ejecuta la "funtion2" -->
  </div>

</template>

<script>
export default {
  name: "Ejemplo",
  data(){ //donde se guardan todas las variables
    return{
      variable: "Que pasa gente, estoy DORAMION",
      inputText: "",
      array:["hola", "hola1", "this."]
    }
  },
  methods: { //donde se guardan todos los metodos
    funtion2(){//cambia la variable "variable" a "funtion2"
      this.variable = "funtion2"
    },
    funtion1(){//cambia la variable "variable" a "funtion1"
      this.variable = "funtion1"
    }
  },
  computed: { //funciones para editar variables sin perder la variable original

  }, 
  watch:{ //para ejecutar funciones cuando cambie alguna variable
    variable: function () { //imprime por consola cada vez que se cambia la variable "variable"
      console.log("Variable cambiada")
    }
  }
}
</script>

<style>

</style>