<template>
  <div class="home-view-container">
    <h1>NBA Playoffs 2019</h1>

    <router-link :to="`/games/lac-gsw`">
      Los Angeles Clippers vs Golden State Warriors
    </router-link>

    <router-link :to="`/games/uta-hou`">
      Utah Jazz vs Houston Rockets
    </router-link>

    <router-link :to="`/games/por-okc`">
      Portland Trailblazers vs Oklahoma City Thunder
    </router-link>

    <router-link :to="`/games/den-sas`">
      Denver Nuggets vs San Antonio Spurs
    </router-link>

    <router-link :to="`/games/mil-det`">
      Milwaukee Bucks vs Detroit Pistons
    </router-link>

    <router-link :to="`/games/bos-ind`">
      Boston Celtics vs Indiana Pacers
    </router-link>

    <router-link :to="`/games/phi-bkn`">
      Philadelphia 76ers vs Brooklyn Nets
    </router-link>

    <router-link :to="`/games/tor-orl`">
      Toronto Raptors vs Orlando Magic
    </router-link>

  </div>
</template>

<script>
import { mapActions } from 'vuex'

export default {
  name: 'home',
  data () {
    return {
    }
  },
  methods: {
    ...mapActions([
      'addPet'
    ])
  }
}
</script>
