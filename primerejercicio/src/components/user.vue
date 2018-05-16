<template>
<div class="users">
    <h1>User component</h1>
    <ul>
      <li v-for="(user, index) in users" :key="index">
         {{user.name}}-{{user.email}}
      </li>
    </ul>
    <form v-on:submit.prevent="agregar">
      <input type="text" v-model="newuser.name" placeholder="Name">
      <input type="email" v-model="newuser.email" placeholder="Email">
      <button >
        agregar
      </button>
    </form>
</div>
</template>

<script>
export default {
  data(){

    return{
      users: [
        {
          name: 'nefeli',
          email: 'nefeli@hotmail.com',
          contacto:false
        },
        {
          name: 'rocio',
          email: 'rocio@hotmail.com',
          contacto:true
        },
        {
          name: 'maria',
          email: 'maria@hotmail.com',
          contacto:false
        },
      ],
    newuser: {

    }
    }
  },
  methods:{
    agregar(){
      this.users.push(this.newuser);
      this.newuser = "";
    }

  }

}
</script>

<style>
 .users {
   background-color: black;
   color:beige;
   font-family: 'Courier New', Courier, monospace;
   padding: 20px;
 }

</style>


