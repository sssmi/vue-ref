<template>
  <div id="app">
    <h1>Your Upcoming Destinations</h1>
    <div class="location-contain">
      <div class="locations">
        <div v-for="location in locations">
          <place 
            :name="location.name" 
            :img="location.img" 
            :description="location.desc" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Place from './components/Place.vue';
export default {
  name: 'App',
  components: {
    Place
  },
  data() {
    return {
      locations: [
        {
          name: 'moscow',
          img: 'https://s3-us-west-2.amazonaws.com/s.cdpn.io/28963/moscow.svg',
          desc: `Moscow is the capital and most populous city of Russia, with 
          13.2 million residents within the city limits and 17.8 million within 
          the urban area. Moscow has the status of a Russian federal city.`
        },
        {
          name: 'paris',
          img: 'https://s3-us-west-2.amazonaws.com/s.cdpn.io/28963/paris1.svg',
          desc: `Paris is the capital and most populous city of France. By 
          the 17th century, Paris was one of Europe's major centres of finance, 
          commerce, fashion, science, and the arts, and it retains that position still today.`
        },
        {
          name: 'rome',
          img: 'https://s3-us-west-2.amazonaws.com/s.cdpn.io/28963/rome.svg',
          desc: `Rome's history spans more than 2,500 years. While Roman mythology 
          dates the founding of Rome at around 753 BC, the site has been inhabited 
          for much longer, making it one of the oldest continuously occupied sites
           in Europe.`
        },
        {
          name: 'paris',
          img: 'https://s3-us-west-2.amazonaws.com/s.cdpn.io/28963/paris2.svg',
          desc: `Paris is the capital and most populous city of France. By the 
          17th century, Paris was one of Europe's major centres of finance, commerce, 
          fashion, science, and the arts, and it retains that position still today.`
        }
      ]
    };
  }
};
</script>

<style>
body {
  width: 100vw;
  height: 100vh;
  font-family: 'NTR', sans-serif;
  background: #eee;
  font-size: 16px;
}

h1 {
  text-align: center;
}

.location-contain {
  display: flex;
  justify-content: center;
}

img {
  margin: 10px;
  align-self: center;
}

h2 {
  text-transform: capitalize;
  margin: 0;
  text-align: center;
}
</style>
