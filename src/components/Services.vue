<template>
  <section id="services" class="overflow-hidden">


    <v-row no-gutters>
      <v-col class="hidden-sm-and-down" md="6">
        <v-img :src="require('@/assets/services.png')" height="100%"/>
      </v-col>

      <v-col class="text-center pa-5" cols="12" md="6">
        <v-row class="fill-height" align="center" justify="center">
          <v-col cols="12">
            <base-bubble-2 style="transform: translateX(55%)"/>

            <base-heading class="info--text">
              Mis Servicios
            </base-heading>

            <base-text class="mb-5">
              Cuento con la capacidad para ofrecerle soluciones de acuerdo a sus necesidades en las siguientes areas:<br>
            </base-text>
          </v-col>

          <v-col v-for="(service, i) in services" :key="i" class="text-center mb-3" md="6">
            <v-avatar class="elevation-6 mb-2" color="#69A1BB" size="64" tile>
              <v-icon dark size="52" v-text="service.icon"/>
            </v-avatar>

            <base-text>
              <div class="mb-2" v-text="service.name"/>
              <div v-html="service.blurb" />
            </base-text>
          </v-col>

        </v-row>
      </v-col>
    </v-row>
  </section>
</template>

<script>
  export default {
    name: 'Services',
    isIntersecting: false,

    data: () => ({
      services: [
        {
          name: 'Diseño web',
          icon: 'mdi-web',
          blurb: 'Diseño de paginas web adaptativas. ',
        },
        {
          name: 'Programación web',
          icon: 'mdi-code-braces',
          blurb: 'Desarollo de aplicaciones en la nube.',
        },
        {
          name: 'Macros VBA Excel',
          icon: 'mdi-microsoft-excel',
          blurb: 'Desarrollo de aplicaciones macro para automatización de procesos en excel.',
        },
        {
          name: 'Hosting',
          icon: 'mdi-server',
          blurb: 'Administración de hostings webs (CPANEL).',
        },
      ],
    }),
  }
</script>
