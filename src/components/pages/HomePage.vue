<template lang="pug">
div
  <v-container grid-list-md>
    <v-layout row wrap fill-width>
      <FeederCheckinsMap :duration='duration' class='xs12' height='400px'/>
      <Leaderboard :duration='duration' class='xs3'/>
      <v-flex xs9>
        <v-card>
          div(style='padding-left: 5px;')
            span This website is under development.
            h1 Code for dinosaurs
            h4 Meetings are Tuesday at noon in the CS lab (JXJ 2311).
            a(href="https://sites.google.com/view/alecrlindsay/research/jp-chickadee-project") check out the biology website for more information <br>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
import Api from '@/api';
import FeederCheckinsMap from '@/components/molecules/FeederCheckinsMap';
import Leaderboard from '@/components/molecules/Leaderboard';

export default {
  name: 'HelloWorld',
  components: {
    FeederCheckinsMap,
    Leaderboard,
  },
  props: {
    duration: {
      type: String,
      required: true,
    },
  },
  data() {
    return {};
  },
  created() {
    console.log(`duration is ${this.duration}`);
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

</style>