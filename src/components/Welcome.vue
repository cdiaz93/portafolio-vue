<template>
  <section
    id="welcome"
    class="overflow-hidden"
  >
    <v-row no-gutters>
      <v-col class="hidden-sm-and-down" md="6">
        <v-img :src="require('@/assets/welcome2.jpg')" height="100vh"/>
      </v-col>

      <v-col class="align-content-space-between layout wrap" cols="12" md="6" :pa-5="$vuetify.breakpoint.smAndDown">

        <base-bubble-1 style="transform: rotate(180deg) translateY(25%)"/>

        <v-row align="center" justify="center">
          <v-col cols="10" md="7">
            <base-heading>Bienvenido!</base-heading>
            <base-text>
              Te doy una cordial bienvenida a mi portafolio.<br>
              Por este medio podras observar todas mis ideas, proyectos, y conocer mas sobre mi.
              <br><br>
              Gracias por tu visita:
            </base-text>
             <br>
            <base-btn class="mt-4" @click="$vuetify.goTo(target('#recent-projects'), options)">
              Empecemos
            </base-btn>
          </v-col>
        </v-row>

        <base-bubble-2
          style="transform: rotate(180deg) translate(-200px, -15%)"
        />
      </v-col>
    </v-row>
  </section>
</template>

<script>

  // animaciones srolling: https://vuetifyjs.com/en/features/scrolling/ 
  import * as easings from 'vuetify/lib/services/goto/easing-patterns'

  export default {
    data () {
      return {
        type: 'selector',
        number: 1000,
        selector: '#recent-projects',
        duration: 2000,
        offset: 0,
        easing: 'easeInOutCubic',
        easings: Object.keys(easings),
      }
    },
    methods:{
      target (val) {
        if (!isNaN(val)) return Number(val)
        else return val
      },
    },
    computed: {
      options () {
        return {
          duration: this.duration,
          offset: this.offset,
          easing: this.easing,
        }
      },
      element () {
        if (this.selected === 'Button') return this.$refs.button
        else if (this.selected === 'Radio group') return this.$refs.radio
        else return null
      },
    },
  }
</script>

