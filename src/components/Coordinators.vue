<template>
    <div>
        <v-row>
            <!-- <v-col><h1 :class="$vuetify.breakpoint.name == 'xl' || $vuetify.breakpoint.name == 'lg' ? 'h1-xl' : 'h1-xs'">
            Nuestras coordinadoras
            </h1></v-col> -->
        </v-row>
       <div class="container-cards-coordinators">

       </div>
       <v-row>
        <v-div
        class="container-card-photo"
        v-for="(card, index) in cards"
        :key="index">
        <v-card class="card-photo-coordinator" flat @click="descriptionVisible(card.name, card.description, card.src)">
            <img class="img-card" :src="card.src" alt="">
            <div class="banner-card-photo">
              <span class="span-name-card">{{card.name}}</span>
            </div>
        </v-card>
    </v-div>
       </v-row>
       <v-row>
        <div class="card-description" v-if="description.isVisible">
          <span class="span-name-description"
          
          >{{description.name}}</span>
          <img class="photo-description" :src="description.src" alt="">
          <span class="span-description">{{description.description}}</span>
        </div>
       </v-row>
        <!-- <div class="container-card-photo"
        v-for="(card, index) in cards"
        :key="index">
            <v-card class="card-photo-coordinator">
            <v-parallax :src="card.src"></v-parallax>
            </v-card>
        </div> -->
           
    </div>
</template>
<script>

    export default {
        name: 'coordinators',
        components: {},
        data: () => ({
            cards: [
          {
            src: require('../assets/Tere.png'),
            name: 'Teresa Mojica',
            description: 'Aqui va la descripcion.'
          },
          {
            src: require('../assets/Gema.png'),
            name: 'Gema Tabares',
            description: 'Aqui va la descripcion.'
          },
          {
            src: require('../assets/Paty.png'),
            name: 'Paty Bazan',
            description: 'Aqui va la descripcion.'
          },
          {
            src: require('../assets/Mirna.png'),
            name: 'Mirna',
            description: 'Aqui va la descripcion.'
          },
          {
            src: require('../assets/Mirsa.png'),
            name: 'Mirsa Santos',
            description: 'Aqui va la descripcion.'
          },
        ],
        description: {
          isVisible: false,
          name: '',
          description: '',
          src: ''
        }
        }),
      methods:{
          descriptionVisible(name, description, src){
            this.description.isVisible = true,
            this.description.name = name,
            this.description.description = description,
            this.description.src = src
          }
        }
    }

</script>

<style>
.h1-xl{
  font-size: 6vw;
  color:#601F7F;
  text-align: center;
  position: absolute;
  top: 43%;
  left: 12vw;
  right:12vw;
}

.h1-xs{
  font-size: 5vw;
  color:#601F7F;
  text-align: center;
  position: absolute;
  top: 43%;
  left: 10vw;
  right:10vw;
}

.card-photo-coordinator{
    width: 19vw;
    height:100%;
    left:3vw;
}

.img-card{
    width: 100%;
    margin: 1vw;
}

.container-card-photo{
    display: flex;
    flex-direction: row;
}

.banner-card-photo{
  background-color: rgba(146,63,177, .5);
  position:absolute;
  top: 60%;
  height: 34%;
  width: 100%;
  left:1vw;
}

.span-name-card{
  font-size: 3.5vw;
  color:aliceblue;
  margin: 1vw;
  line-height: 1;
}
.card-description{
  background-color: rgba(193,166,203);
  top: 105%;
  width: 80vw;
  height: 85vh;
  position:absolute;
  left:10vw;
  display: flex;
  justify-content: center;
}
.span-name-description{
  font-size: 6vw;
  color:white;
  margin: 1vw;
  text-align: center;
}
.photo-description{
  position: absolute;
  width: 18vw;
  top:25%;
  left:8vw;
  margin: 1vw;
  border: 2px solid white;
}

.span-description{
  position:absolute;
  line-height: 1;
  top:25%;
  left:30vw;
  right: 4vw;
  font-size: 1.7vw;
  color: white;
  z-index: 1;
}
</style>