<template>
  <v-app-bar
    v-scroll="onScroll"
    :color="!isScrolling ? 'transparent' : 'white'"
    fixed
    flat
  >
    <v-slide-x-transition>
      <v-img v-if="showLogo"
        :src="require('@/assets/logo1.png')"
        class="shrink"
        contain
        height="50"
        width="260"
      />
       
      
    </v-slide-x-transition>
    
        
     
    <v-spacer />
     <v-tabs v-if="showLogo" class="shrink" centered>
       <v-tab   @click="$vuetify.goTo(target('#recent-projects'), options)">Proyectos</v-tab>
        <v-tab  @click="$vuetify.goTo(target('#services'), options)">Servicios</v-tab>
        <v-tab  @click="$vuetify.goTo(target('#about'), options)">Sobre mi </v-tab>
        <v-tab  @click="$vuetify.goTo(target('#get-in-touch'), options)">Contacto </v-tab>
      </v-tabs>
  </v-app-bar>
</template>

<script>
  // animaciones srolling: https://vuetifyjs.com/en/features/scrolling/ 
  import * as easings from 'vuetify/lib/services/goto/easing-patterns'

  export default {
    name: 'CoreAppBar',

    components: {
      // SocialMedia: () => import('@/components/SocialMedia'),
    },

    data: () => ({
      showLogo: false,
      isScrolling: false,
      type: 'selector',
      number: 1000,
      selector: '#recent-projects',
      duration: 2000,
      offset: 0,
      easing: 'easeInOutCubic',
      easings: Object.keys(easings),
    }),

    methods: {
      onScroll () {
        const offset = window.pageYOffset
        this.isScrolling = offset > 50
        this.showLogo = offset > 200
      },

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
    },
  }
</script>
