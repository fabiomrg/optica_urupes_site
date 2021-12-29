<template>
  <section id="hero">
    <v-img
      :min-height="minHeight"
      :src="require('@/assets/light3.jpg')"
      class="white--text"
      gradient="to bottom, rgba(20, 20, 20, .1), rgba(0,0,0,.3)"
    >
      <v-container class="px-2 py-0">
        <v-responsive
          class="d-flex align-center mx-auto"
          height="50%"
          max-width="800"
          width="90%"
        >
        <br/><br/><br/>
        <v-card class="rounded-xl" color="#0000007D">
          <br/><br/>
          <v-row class="mx-6" align="center">
            <base-subheading
            size="text-h5"
            weight="regular"
            title="Há 30 anos com a saúde dos seus olhos em primeiro lugar!"/>
            <base-body >
              <p class="text-white">Sabemos da importância da saúde dos olhos e o quanto nossos clientes são especiais para nós. Por isso temos tanto cuidado e carinho com nossos produtos, para que realmente satisfaça nosso público.</p>
              <p class="text-white">Trazemos sempre o que há de mais moderno na confeccão de nossos óculos, muitas opções com as melhores marcas do mercado. Aqui você vai encontrar desde o conforto de uma lente com alta tecnologia e também uma armação que te traga beleza e elegância.</p> 
              <p class="text-white">Se ainda não conhece nossa loja, venha! Estamos prontos a atendê-los.</p>
              <p class="text-white">Equipe Óptica Urupês </p>
           </base-body>
          </v-row>
        </v-card>
        <br/><br/><br/><br/>
        </v-responsive>
      </v-container>
    </v-img>
  </section>
</template>

<script>
  export default {
    name: 'SectionHero',

    provide: {
      theme: { isDark: true },
    },

    computed: {
      minHeight () {
        const height = this.$vuetify.breakpoint.mdAndUp ? '50vh' : '25vh'

        return `calc(${height} - ${this.$vuetify.application.top}px)`
      },
    },
  }
</script>
<style type="text/css">
  rounded-card{
      border-radius:60;
  }
  p{
      color:white;
  }

</style>
