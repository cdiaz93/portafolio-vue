<template>
  <section id="get-in-touch" class="overflow-hidden">
    <v-row class="black--text" no-gutters>
      <v-col class="hidden-sm-and-down" md="6">
        <v-img :src="require('@/assets/contact.png')" height="100%" />
      </v-col>

      <v-col class="pa-5" cols="12" md="6">
        <base-bubble-1 />

        <base-heading class="mb-5">
          Contacto
        </base-heading>

        <base-text class="mb-7 text-justify">
          Si tienes inquietudes, o te interesa empezar algun trabajo conmigo puedes contactarme por los siguientes medios:

          <br><br>

          <v-avatar class="elevation-6 mb-2" color="#69A1BB" size="55" tile>
            <v-icon color="white" size="50">mdi-whatsapp</v-icon>
          </v-avatar>
           <span class="pl-2"> <b>(57) 312 7840675 </b>  </span> 
          <br>
          <v-avatar class="elevation-6 mb-2" color="#69A1BB" size="55" tile>
            <v-icon color="white" size="50">mdi-email-edit-outline</v-icon>
          </v-avatar>
           <span class="pl-2"> <b> carl894@hotmail.com </b> </span> 
          <br>
          <v-avatar class="elevation-6 mb-2" color="#69A1BB" size="55" tile>
            <v-icon color="white" size="50">mdi-linkedin</v-icon>
          </v-avatar>
          <span class="pl-2"> <b> <a href="https://www.linkedin.com/in/carlos-david-diaz-mosquera-47297b135" target="_blank">Perfil Linkedin </a>  </b> </span> 
          <br>
          <v-avatar class="elevation-6 mb-2" color="#69A1BB" size="55" tile>
            <v-icon color="white" size="50"> mdi-account-box-multiple</v-icon>
          </v-avatar>
          <span class="pl-2"> <b> <a href="https://interacpedia.com/user/carlos-diaz-3" target="_blank">Perfil Interacpedia </a>  </b> </span> 

          

         
                  
         
        </base-text>

        


        <!-- <v-icon x-large v-text="mdi-web"/> -->

      </v-col>
    </v-row>
  </section>
</template>

<script>
  export default {
    name: 'GetInTouch',
  }
</script>
