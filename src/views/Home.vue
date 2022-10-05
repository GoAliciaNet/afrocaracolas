<template>
  <div>
    <HeaderBar/>
    <v-carousel>
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
      reverse-transition="fade-transition"
      transition="fade-transition"
    ></v-carousel-item>
  </v-carousel>
  <div class="container-img">
  <img src="../assets/waves.png" alt="" class="img-cover">
  <v-row>
    <v-col><h1 :class="$vuetify.breakpoint.name == 'xl' 
    || $vuetify.breakpoint.name == 'lg' ? 'h1-xl' : 'h1-xs'">
      ¿Qué es Afrocaracolas?
    </h1></v-col>
    <v-col xl="1" lg="1"></v-col>
    <v-col xl="3" lg="3" md="3">
      <img 
    src="../assets/logo-afrocaracolas.png" alt="Logo afrocaracolas"
    class="container-img__logo"
    >
    <p class="container-img__text">Somos mujeres Afromexicanas trabajamos 
      directamente en las comunidades afromexicanas de Guerrero y Coahuila para recuperar, 
      fortalecer y preservar la identidad del Pueblo Afromexicano</p>
    </v-col>
  </v-row>
  <div class="banner-purple">
    <div class="col-text-center">
        <h4>LUCHAMOS CONTRA EL RACISMO Y LA DISCRIMINACIÓN </h4>
    </div>
  </div>
  </div>
   <OurWork/>

   <Footer/>
   
  </div>
</template>

<script>
import OurWork from "../components/OurWork.vue";
import Footer from "../components/Footer.vue";
import HeaderBar from "../components/HeaderBar.vue";
// @ is an alias to /src

export default {
  name: 'Home',
  components: {
    OurWork,
    Footer,
    HeaderBar
},
  data: () => ({
    menus:[
      {text: '¿Quienes somos?', path: '/somos'},
      {text: 'Escuela de formación antirracista', path: ''},
      {text: '¿Blog', path: ''},
      {text: 'Estadistica', path: ''},
      {text: 'Contacto', path: ''},
    ],
    items: [
          {
            src: require('../assets/portada-museo.png'),
          },
          {
            src: require('../assets/portada-cg.png'),
          },
          {
            src: require('../assets/portada-nacimiento.png'),
          },
          {
            src: require('../assets/portada-playa.png'),
          },
        ],
      }),
  mounted(){
    // console.log(this.$vuetify.breakpoint.lg)
    // console.log(this.$vuetify.breakpoint.md)
    // console.log(this.$vuetify.breakpoint.sm)
    // console.log(this.$vuetify.breakpoint.xs)
    // console.log(this.$vuetify.breakpoint)
  }
}
</script>
<style scoped>
.logo{
  width: 65px;
}
a{
  text-decoration: none;
  color: white !important;
  font-size: 1.25rem;
  line-height: 1;
}
.bar__col{
  display: flex;
  align-items: center;
}
.bar__col--right{
  display: flex;
  align-items: center;
  justify-content: flex-end;
}
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
  font-size: 7vw;
  color:#601F7F;
  text-align: center;
  position: absolute;
  top: 5%;
  left: 10vw;
}

.h1-xs{
  font-size: 6vw;
  color:#601F7F;
  text-align: center;
  position: absolute;
  top: 5%;
  left: 16vw;
}
.container-img__logo{
  width: 30%;
  position: absolute;
  top: 18%;
  left:5%;
}
.container-img__text{
  position: absolute;
  top: 20%;
  left: 35%;
  right: 5%;
  transform: translate(-50% -50%);
  color: #00649E;
  font-size: 4vw;
  line-height: 1;
}
.banner-purple{
  background-color: #601F7F;
  opacity: .5;
  position:absolute;
  top: 60%;
  /* padding: 5px; */
}

h4{
  color:#fff;
  font-size:4vw;
  right: 20%;
  left: 20%;
  line-height: 1;
  text-align: center;
  margin: 10px 0 10px 0
}
.col-text-center{
  display: flex;
  justify-content: center;
}
.menu-text-item{
  color: black;
}
</style>
