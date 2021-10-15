<template>

  <section id="recent-projects" class="overflow-hidden">
    
    <v-row no-gutters>
      <v-col class="text-center pa-5 white--text" cols="12" md="12">
        <base-bubble-1 style="transform: rotate(180deg) translateX(25%)"/>

        <base-heading>
          Proyectos recientes
        </base-heading>

        <base-text class="mb-5">
          Estos son algunos de los trabajos que he realizado en mi trayecto como profesional.<br>
        </base-text>

        <v-card color="rgb(77 67 61 / 0%) !important" cols="10" md="6">
          <v-container class="pa-2">
            <v-row>
              <v-col v-for="project in projects" :key="project.image" cols="12" md="6">
                <a :href="project.link" class="text-decoration-none" target="_blank">
                  <v-img :src="require(`@/assets/projects/${project.image}.jpg`)" max-height="350"> 
                    <v-card class="white--text rounded-0" color="rgb(77 67 61 / 70%) !important">  {{project.name}}  </v-card > 
                  </v-img>
                </a>
              </v-col>
            </v-row>
          </v-container>
        </v-card>
      </v-col>

    </v-row>
   
  </section>

</template>

<style scoped>
  #recent-projects {
    background: url('../assets/background1.jpg') no-repeat center center fixed !important;
    background-size: cover;

  }
</style>

<script>
  export default {
    name: 'RecentProjects',

    data: () => ({
      projects: [
        { name: "Proyecto Imaster / Ciclo-3 Grupo-48" , image: 'project1', link:'https://imastertours.herokuapp.com/' }, 
      ],
    }),
  }
</script>
