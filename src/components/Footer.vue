<template>
  <v-footer
    color="#601F7F"
  >
    <v-card
      class="flex"
      flat
      color="#601F7F"
    >
    <v-row>
    <v-col lg="2" md="2">
    <img 
    src="../assets/logo-afrocaracolas.png" alt="Logo afrocaracolas"
    :class="$vuetify.breakpoint.width > 800 ? 'container-img__logo' : 'container-img__logo--mobile'"
    >
      </v-col>
      <v-col lg="4" md="4">
        <p>Sigue nuestras redes</p>
        <v-btn
          v-for="contact in mediaItems"
          :key="contact"
          class="mx-4"
          dark
          icon
          :href="contact.src"
          target="_blank"
        >
          <v-icon size="24px">
            {{ contact.icon }}
          </v-icon>
        </v-btn>
      </v-col>
      <v-col lg="3" md="3">
        <div class="container-inputs">
        <v-text-field
          dense
          class="input-form"
          label="Nombre"
          solo
        ></v-text-field>
        <v-text-field
          class="input-form"
          dense
          label="Correo electrónico"
          solo
        ></v-text-field>
        </div>
      </v-col>
      <v-col lg="3" md="3" class="container-text-area">
        <v-textarea
          solo
          name="input-7-4"
          label="Escribe aqui tu comentario"
          height="80px"
        ></v-textarea>
        <v-btn
        color="#00649E"
        >Enviar</v-btn>
      </v-col>
    </v-row>
    </v-card>
  </v-footer>
</template>
<script>
  export default {
    data: () => ({
      mediaItems: [
        {
          icon: 'mdi-facebook', 
          src: 'https://www.facebook.com/Afrocaracolas-Saberes-itinerantes-105966055020129'
        },
        {
          icon: 'mdi-twitter', 
          src: 'https://twitter.com/afrocaracolas'
        },
        {
          icon: 'mdi-instagram', 
          src: 'https://www.instagram.com/afrocaracolas/'
        },
      ],
    }),
  }
</script>

<style scoped>
.container-img__logo{
  width: 100px;
}
.container-img__logo--mobile{
  width: 50px;
}
.container-inputs{
  display: flex;
  flex-direction: column;
}
.input-form{
  margin: 4px;
}
p{
  color: white;
  font-size: 1rem;
  margin: none;
  text-align: center;
  padding: none;
}
.container-text-area{
  display: flex;
  flex-direction: column;
  justify-content: center;
}
</style>
