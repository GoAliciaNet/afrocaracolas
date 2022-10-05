<template>
  <div>
    <div class="container-background-white"></div>
   <h2>Nuestro trabajo</h2>
   
   <v-row>
    <v-col lg="4" md="4" v-for="(info, key) in infoCards"
    :key="key">
    <v-card
    class="mx-auto my-12"
    max-width="374"
  >
    <!-- <template slot="progress">
      <v-progress-linear
        color="deep-purple"
        height="10"
        indeterminate
      ></v-progress-linear>
    </template> -->

    <v-img
      height="200"
      :src="info.src"
    ></v-img>

    <v-card-title class="card-title">
      {{info.title}}
    </v-card-title>

    <v-card-text>
      <v-row
        align="center"
        class="mx-0"
      >
      </v-row>
      <p class="card-date">{{info.date}}</p>
      <p class="card-text">
     {{info.text}}
      </p>
    </v-card-text>

    <v-divider class="mx-4"></v-divider>

  
    <!-- <v-card-actions>
      <v-btn
        color="deep-purple lighten-2"
        text
        @click="reserve"
      >
        Reserve
      </v-btn>
    </v-card-actions> -->
  </v-card>
    </v-col>
   </v-row>

  </div>
</template>

<script>
  export default {
    data: () => ({
      loading: false,
      selection: 1,
      infoCards:[
      {
          title: 'Shirley Campbell visita Acapulco y se reune con Afrocaracolas',
          text:'Cuando Shirley Campbell nombra su herencia africana, nos confirma que también el amor cuenta para reapropiarnos de nuestra identidad...',
          date: '03 octubre de 2022',
          src: require('../assets/shirley.jpg'),
      },
      {
          title: 'Trabajamos en la Asamblea-Tallercita "Identidad afromexicana y Derechos Humanos" ',
          text:'en la comunidad El Capricho de municipio de Ometepec y tuvimos el honor de contar con Harold Robinson Davis, Cecilia Maurente, Ivan Castellanos del UNFPA...',
          date: '30 septiembre de 2022',
          src: require('../assets/capricho.jpg'),
      },
      {
          title: '¡La representación de las personas negras y afrodescendientes sí importa y el cómo se nos presenta aún más!' ,
          text:'Hemos crecido jugando con muñecas que no se parecían a nosotras y regalámos a nuestras hijas las mismas barbies blancas, y ahora que somos conscientes....',
          date: '27 de septiembre de 2022',
          src: require('../assets/representacion.jpg'),
      },
      {
          title: 'Trabajamos en la Tallercita: "Avances y obstáculos en la participación política y comunitaria de las Mujeres Negras Maskogas".',
          text:'Desde el Museo Afromexicano de Huehuetán, Guerrero, la organización Afrocaracolas conmemoraron el 31 Día Internacional de los Afrodescendientes con una Asamblea y un Taller de Identidad Afromexicana donde difundieron...',
          date: '24 de septiembre de 2022',
          src: require('../assets/coahuila.jpg'),
      }
      ,{
          title: 'Participamos en el encuentro que se realizó en Bracketville, Texas para conmemorar el Día de los Seminoles y honrar la lucha de los Black Seminoles.',
          text:'Como mujeres cimarronas y jovenas, nos llena de entusiasmo este acto histórico porque nos motiva a preservar la identidad Negra Maskoga desde nuestros cantos ancestrales, tradiciones, costumbres y conocimientos...',
          date: '21 de septiembre de 2022',
          src: require('../assets/seminol.jpg'),
      },
      {
          title: 'Conmemoramos el Día Internacional de las personas Afrodescendientes con trabajo territorial y colectivo',
          text:'Desde el Museo Afromexicano de Huehuetán, Guerrero, la organización Afrocaracolas conmemoraron el 31 Día Internacional de los Afrodescendientes con una Asamblea y un Taller de Identidad Afromexicana donde difundieron...',
          date: '31 de agosto de 2022',
          src: require('../assets/portada-museo.png'),
      },
      ]
    }),

    methods: {
      reserve () {
        this.loading = true

        setTimeout(() => (this.loading = false), 2000)
      },
    },
  }
</script>

<style scoped>
.container-background-white{
  height:30px;
  background-color:#fff;
}

h2{
  text-align: center;
  font-size: 3rem;
  color: #601F7F;
}
.card-title{
  line-height: 1.2;
  color:#601F7F;
}
.card-date{
  margin-top: 10px;
  color: grey;
  text-align: right;
}
.card-text{
  text-align: justify;
  line-height: 1.4;
}
</style>
