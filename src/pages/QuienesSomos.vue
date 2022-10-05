<template>
    <div>
        <HeaderBar/>
        <div class="container-img">
  <img src="../assets/waves.png" alt="" class="img-cover">
  <v-row>
    <v-col><h1 :class="$vuetify.breakpoint.name == 'xl' 
    || $vuetify.breakpoint.name == 'lg' ? 'h1-xl' : 'h1-xs'">
      ¿Qué es Afrocaracolas?
    </h1></v-col>
    <v-col xl="3" lg="3" md="3">
    <p class="container-img__text">Somos mujeres negras y afrodescendientes que trabajamos directamente en las comunidades
        afromexicanas de Guerrero y Coahuila para recuperar, fortalecer y preservar la identidad del Pueblo Afromexicano.
    <ul>
        <li>Promovemos la participación política de las mujeres
            afromexicanas e impulsamos proyectos de autonomía económica
        </li>
        <li>Facilitamos tallercitas de identidad afromexicana y derechos humanos
        </li>
    </ul>
    </p>

    </v-col>
  </v-row>
  <div class="banner-purple">
    <!-- <div class="col-text-center"> -->
        <h3 class="text-title">Porque venimos del mar </h3>
        <div class="container-logo-text">
            <p class="text-banner-left">Somos mujeres Afromexicanas trabajamos directamente en las comunidades afromexicanas
            de Guerrero y Coahuila para recuperar, fortalecer y preservar la identidad del pueblo Afromexicano
            </p>
        <img 
            src="../assets/logo-afrocaracolas.png" alt="Logo afrocaracolas"
            class="container-img__logo"
        >
        </div>
    </div>
  </div>
  <Coordinators/>
</div>
</template>
<script>
import Coordinators from '../components/Coordinators.vue'
import HeaderBar from '../components/HeaderBar.vue'


export default {
    name: 'QuienesSomos',
    components: {
        HeaderBar,
        Coordinators,
    },
    data: () => ({

    })
}
</script>
<style scoped>
.container-img{
  position: relative;
  display: inline-block;
  text-align: center;
  width:100%;
}

.img-cover{
  width: 100%;
}
.h1-xl{
  font-size: 6vw;
  color:#601F7F;
  text-align: center;
  position: absolute;
  top: 3%;
  left: 12vw;
  right:12vw;
}

.h1-xs{
  font-size: 5vw;
  color:#601F7F;
  text-align: center;
  position: absolute;
  top: 3%;
  left: 10vw;
  right:10vw;
}
.container-img__text{
  position: absolute;
  top: 12%;
  left: 15%;
  right: 15%;
  transform: translate(-50% -50%);
  color: #00649E;
  font-size: 2.5vw;
  line-height: 1;
}

.banner-purple{
  background-color: #C1BFD2;
  position:absolute;
  top: 52%;
  width: 90%;
  height: 75vh;
  opacity:.8;
  right: 5%;
  left: 5%;
}
.col-text-center{
  display: flex;
  /* justify-content: center; */
  flex-direction: column;
}
.text-title{
  color:#601F7F;
  font-size:4vw;
  right: 20%;
  left: 20%;
  line-height: 1;
  text-align: center;
  margin: 10px 0 10px 0
}

.container-img__logo{
  width: 20vw;
  top: 100%;
  height: 20vw;
  margin:1vw;
}
.container-logo-text{
    display: flex;
    flex-direction: row;
}
.text-banner-left{
  width: 60%;
  right:40%;
  left:5%;
  font-size: 3vw;
  line-height: 1.1;
  color: #00649F;
  margin:3vw;
/* 
  color:#601F7F;
  font-size:4vw;
  right: 20%;
  left: 20%;
  line-height: 1;
  text-align: center;
  margin: 10px 0 10px 0 */
}
</style>