<template>
  <div class="home-view-container">
    <h1>NBA Playoffs 2019</h1>
    <div class="games-container">
      <div class="logos-container">
        <router-link :to="`/games/lac-gsw`">
          <img src="@/assets/teams-logos/clippers.png"/>
          <img src="@/assets/teams-logos/warriors.png"/>
        </router-link>
      </div>

      <div class="logos-container">
        <router-link :to="`/games/uta-hou`">
          <img src="@/assets/teams-logos/jazz.jpg"/>
          <img src="@/assets/teams-logos/rockets.png"/>
        </router-link>
      </div>

      <div class="logos-container">
        <router-link :to="`/games/por-okc`">
          <img src="@/assets/teams-logos/portland.png"/>
          <img src="@/assets/teams-logos/thunder.jpeg"/>
        </router-link>
      </div>

      <div class="logos-container">
        <router-link :to="`/games/den-sas`">
          <img src="@/assets/teams-logos/nuggets.png"/>
          <img src="@/assets/teams-logos/spurs.jpg"/>
        </router-link>
      </div>

      <div class="logos-container">
        <router-link :to="`/games/mil-det`">
          <img src="@/assets/teams-logos/bucks.jpeg"/>
          <img src="@/assets/teams-logos/pistons.png"/>
        </router-link>
      </div>

      <div class="logos-container">
        <router-link :to="`/games/bos-ind`">
          <img src="@/assets/teams-logos/celtics.png"/>
          <img src="@/assets/teams-logos/pacers.png"/>
        </router-link>
      </div>

      <div class="logos-container">
        <router-link :to="`/games/phi-bkn`">
          <img src="@/assets/teams-logos/76ers.png"/>
          <img src="@/assets/teams-logos/nets.jpeg"/>
        </router-link>
      </div>

      <div class="logos-container">
        <router-link :to="`/games/tor-orl`">
          <img src="@/assets/teams-logos/toronto.jpg"/>
          <img src="@/assets/teams-logos/magic.png"/>
        </router-link>
      </div>
    </div>

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
