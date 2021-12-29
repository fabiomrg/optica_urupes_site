<template>
  
    <v-app-bar
      id="home-app-bar"
      app
      elevation="1"
      :height="barHeight"
      color="#f9e754"
      >
        <home-menu/>

         <v-container>
        
          <v-row justify="center">
            
                <base-img  
                  class="mr-3" 
                  contain
                  max-width="120"
                  width="100%"
                  :src="require('@/assets/logo.jpg')"
                
                />
              
            
          </v-row>

          <v-row no-gutters>
            <v-col cols="12" class="text-center">
        
            </v-col>
          </v-row>
        </v-container>
          
         
         
           
        
    </v-app-bar>
 
</template>

<script>
  export default {
    name: 'HomeAppBar',

    data: () => ({
      drawer: null,
      items: [
        'Home',
        'Pro',
      ],
    }),

    components: {
      
      HomeMenu: () => import('@/layouts/home/menu'),
    },
    computed: {
      imageHeight () {
        switch (this.$vuetify.breakpoint.name) {
          case 'xs': return '100px'
          case 'sm': return '200px'
          case 'md': return '100px'
          case 'lg': return '100px'
          case 'xl': return '100px'
        }
      },
      imageWidth () {
        switch (this.$vuetify.breakpoint.name) {
          case 'xs': return '240px'
          case 'sm': return '400px'
          case 'md': return '500px'
          case 'lg': return '500px'
          case 'xl': return '600px'
        }
      },
      barHeight () {
        switch (this.$vuetify.breakpoint.name) {
          case 'xs': return '90px'
          case 'sm': return '100px'
          case 'md': return '100px'
          case 'lg': return '100px'
          case 'xl': return '100px'
        }
      },
    }
  }
</script>

<style lang="sass">
  #home-app-bar
    .v-tabs-slider
      max-width: 24px
      margin: 2 auto

    .v-tab
      &::before
        display: none
</style>
