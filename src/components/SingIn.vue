<template>
    <div class="">
      <div class="box-container">

        <div class="box">
          <img :src="logo" alt="logo" class="logo">
          <p>Esperamos que disfrute navegando y usando nuestra aplicación. En nuestro equipo de desarrollo trabajamos arduamente para crear una plataforma fácil de usar y atravtiva para nuestros
          usuarios. Si tiene algún comentario o sugerencia de cómo podemos mejorar nuestra aplicación para hacerla aún más útil, por favor no dude en hacérnoslo saber.
          </p>
        </div>

        <div class="box1">
          <h1>Log In</h1>
          <div class="labels">
            <label>Username</label><br>
            <InputText type="text" v-model="value" class="dates" />
          </div>
          <div class="labels">
            <label>Password</label><br>
            <InputText type="text" v-model="value" class="dates" />
          </div>
          <button @click="$router.push('/signup')" class="button" style="cursor: pointer;">Login</button>
          <div class="box1-1" rounded>
            <p class="part1">Forgot your password?</p>
            <div class="redes">
              <p class="part1">Or login with:</p>
              <div>
                <Button class="pi pi-facebook" style="cursor: pointer;"></Button>
                <Button class="pi pi-envelope" style="cursor: pointer;"></Button>
                <Button class="pi pi-instagram" style="cursor: pointer;"></Button>
                <Button class="pi pi-twitter" style="cursor: pointer;"></Button>
              </div>
            </div>
          </div>
          <p class="form">New in Vital Check?</p>
            <button @click="$router.push('/register')" class="button" style="cursor: pointer;">Register as a Pharmacy</button>
            <button @click="$router.push('/register')" class="button" style="cursor: pointer;">Register as a Provider</button>
        </div>

        <div class="box2"></div>
      </div>
    </div>
  </template>
  
  <script>

import InputText from 'primevue/components/inputtext/InputText';
import logo from '../assets/logo.png';
import { Button } from 'primevue/button';

export default {
    name: "SingIn",
    data() {
        return {
            logo,
        };
    },
    components: { InputText, Button },
 
};
</script>
  
<style scoped>
body {
  width: 100%;
}
img{
  width: 100%;
  align-items: center;
}
p{
  font-size: 160%;
  text-align: justify;
}
.flex{
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}
.logo{
  margin: auto;
  display: flex;
  justify-content: center; 
  align-items: center; 
}
.box-container{
  display: flex;
}
.box{
  flex: 1;
  padding: 5%;
  align-items: center;
  justify-content: center;
}  
.box1{
  flex:1;
  padding: 5%;
  background-color:#b7334d ;
  margin: 1% 0 0 2%;
  text-align: center;
  color:white;
  border-radius: 10% 0 0 10%;
}
.box2{
  padding: 1.5%;
  margin: 1% 0 0 0;
  background-color: #d96f74;
}
h1{
  font-size: 300%;
  margin: 2% 0 2% 0;
}
.labels
{
  font-size: 150%;
  text-align: justify;
}
.dates{
  width: 100%;
  margin: 2% 0 2% 0;
}
.box1-1{
  justify-content: center;
  align-items: center;
  display: flex;
  flex-direction: column;
}
.button{
  background-color: #d96f74;
  color: white;
  width: 100%;
  margin: 2% 0 2% 0;
  font-size: 150%;
  border: none;
  border-radius: 10px;
  height: 8%;
}
.part1{
  font-size: 130%;
  color: white;
  margin: 2% 0 0 0;
  text-align: center;

}
.redes{
  background: white;
  justify-content: center;
  margin: 2% 0 2% 0;
  color: black; 
  width: 50%;
  height: 200%;
  border-radius: 50px;
}
.redes p{
  color: black;
  font-size: 150%;
  margin: 2% 0 2% 0;
}
button{
  background: none;
  border: none;
  margin: 2% 2% 2% 2%;
  font-size: 300%;
  height: 8%;
}
.form{
  text-align: center;
}
</style>