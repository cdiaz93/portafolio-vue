<template>
  <section id="about" class="overflow-hidden">
    <v-row class="white" no-gutters>
      <v-col class="pa-5" cols="12" md="6">
        <base-bubble-1 style="transform: translate(5%, -5%)" />

        <base-heading class="info--text">
          Acerca de mi
        </base-heading>

        <base-text class="mb-7 text-justify">

          Soy Tecnólogo en Análisis y Desarrollo de Sistemas de Información, tengo conocimiento en varios lenguajes de programación, diseño de paginas web, <br> 
          administración de bases de datos. <br>
          Tambien poseo conocimientos para la realización de mantenimiento preventivo y correctivo a equipos de computo, pero 
          mi enfoque esta más centrado en la programación. <br> <br>
          Me considero una persona: <br>
          Responsable, Alegre, confiable, cordial.<br>
          Que se propone metas y las cumple.<br>
          Me gusta aprender cosas nuevas, estar en constante aprendizaje para crecer como persona y profesionalmente. 
          
          <br><br>
          Siempre dispuesto a ayudar!! .. si es que las condiciones lo permiten.
        </base-text>

        <base-subheading class="info--text">
          Habilidades
        </base-subheading>

        <base-text class="mb-5">
          Estas son mis skills, que me ayudan a cumplir todas mis actividades y labores.<br>
        </base-text>

        <v-alert outlined color="info">
          <v-row v-for="(skill, i) in skills" :key="i" style="color: #69A1BB;">

            <v-col class="text-uppercase" cols="6" v-text="skill.name"/>
            <v-col class="text-right" cols="6" v-text="`${skill.value}%`"/>

            <v-progress-linear :value="skill.value" color="info" height="8"/>
          </v-row>
        </v-alert>
      </v-col>

      <v-col class="hidden-sm-and-down" md="6">
        <v-img :src="require('@/assets/aboutme.png')" height="100%"/>
      </v-col>
    </v-row>
  </section>
</template>

<script>
  export default {
    data: () => ({
      skills: [
        { name: 'PHP / Laravel', value: 100,},
        { name: 'Excel VBA', value: 100,},
        { name: 'NodeJs', value: 80,},
        { name: 'VueJs', value: 80,},
        { name: 'Bootstrap', value: 100,},
        { name: 'MySQL', value: 100,},
        { name: 'MongoDB', value: 80, },
      ],
    }),
  }
</script>
