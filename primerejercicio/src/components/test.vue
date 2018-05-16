<template>
 <div>
   <input type="text" v-model="user.name">
   <h1 v-text="title"></h1>
   <div>{{user.edad}}</div>
   <div v-html="myhtml"> </div>
   <div v-if="showname">
     <p>no puede mostrar nombre</p>
   </div>
   <div v-else>
     <p>Mostrar</p>
   </div>
   <hr>
   <div v-for="(tarea, index) in tareas" :key="index">
     <li>{{tarea.title}}</li>
   </div>
   <button
   v-on:click="saludar(user.name)" >click</button>
   <input type="text" v-on:keyup.enter="valor">
 </div>
</template>
<script>
export default {
  data() {
    return {
      title: 'hola como estan',
      user:{
        name: 'nefeli',
        apellido: 'joñoruco',
        edad: 22
      },
      myhtml: '<h3>como estan</h3>',
      showname: false,
      tareas: [
        {title: 'comer'},
        {title: 'dinner'},
        {title: 'east'},
        {title: 'ffff'},
      ]
    }
  },
  methods:{
    saludar(name){
      alert('hola' + name);
    },

    valor(e){
      console.log('dddd');
    }

  }
}

</script>
<style>

</style>


