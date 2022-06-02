<template>
  <body>
    <div id="evento1">
      <Evento :title="e1_title" :title2="e1_title2" :photo="e1_photo" :general_url="e1_general_url" :tickets_url="e1_tickets_url"
      :prize="e1_prize" :date="e1_date" :location_name="e1_location_name" :location_url="e1_location_url"></Evento>
    </div>
  </body>
</template>

<script>
import Evento from './components/evento.vue'
import e1_photo_ from './assets/Puro_Latino.jpeg'

export default {
    name: 'App',
    components: {
      Evento
    },
    data: function() {
      return {
        e1_title: 'Puro Latino',
        e1_title2: 'Festival',
        e1_photo: e1_photo_,
        e1_general_url: 'https://purolatino.es/sevilla/',
        e1_tickets_url: 'https://purolatino.es/sevilla/entradas/',
        e1_prize: '79 €',
        e1_date: '01/07/22 - 02/07/22',
        e1_location_name: 'Estadio Olímpico de La Cartuja',
        e1_location_url: 'https://goo.gl/maps/RNz2n9qG89YMjcMr5',
      };
    },
  };
</script>

<style>
div#evento1{
width: 348px;
height: 386px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
