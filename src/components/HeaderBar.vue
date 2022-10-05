<template>
    <div>
        <v-app-bar
      color="#601F7F"
      dense
      dark
      height="90px"
    >
  <v-row v-if="$vuetify.breakpoint.width > 700">
  <v-col lg="2" md="2" sm="2" xs="2">
        
    <a href="/"><img src="../assets/logo-afrocaracolas.png" alt="Logo afrocaracolas" class="logo"></img></a>
  </v-col >
      <v-col lg="2" md="2" sm="2" xs="2" class="bar__col">
        <a href="/somos">¿Quienes somos?</a>
      </v-col>
      <v-col lg="2" md="2" sm="2" xs="2" class="bar__col">
        <a href="">Escuela de formación antirracista</a>
      </v-col>
      <v-col lg="2" md="2" sm="2" xs="2" class="bar__col">
        <a href="">Blog</a>
      </v-col>
      <v-col lg="2" md="2" sm="2" xs="2" class="bar__col">
        <a href="">Estadística</a>
      </v-col>
      <v-col lg="2" md="2" sm="2" xs="2" class="bar__col">
        <a href="">Contacto</a>
      </v-col>
    </v-row>
    <v-row v-if="$vuetify.breakpoint.width <=701">
      <v-col class="bar__col--left">
        <img src="../assets/logo-afrocaracolas.png" alt="Logo afrocaracolas" class="logo">
      </v-col>
      <v-col class="bar__col--right">
      <v-menu
        left
        bottom
      >
        <template v-slot:activator="{ on, attrs }">
          <v-btn
            icon
            v-bind="attrs"
            v-on="on"
          >
            <v-icon>mdi-dots-vertical</v-icon>
          </v-btn>
        </template>

        <v-list>
          <v-list-item
            v-for="item in menus"
            :key="item"
            @click="() => {}"
            :to="item.path"
          >
            <v-list-item-content>
              <v-list-item-title v-text="item.text" class="menu-text-item"></v-list-item-title>
            </v-list-item-content>
           
          </v-list-item>
         
        </v-list>
      </v-menu>
    </v-col>
    </v-row>
    </v-app-bar>
    </div>
</template>
<script>
export default {
    name: 'HeaderBar',
    components: {},
    data: () => ({
        menus:[
            {text: '¿Quienes somos?', path: '/somos'},
            {text: 'Escuela de formación antirracista', path: ''},
            {text: '¿Blog', path: ''},
            {text: 'Estadistica', path: ''},
            {text: 'Contacto', path: ''},
        ],
    })
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

</style>