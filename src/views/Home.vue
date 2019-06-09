<template>
  <div class="home-view-container">
    <div class="games-container">
      <div class="logos-container">
        <router-link :to="`/games/lac-gsw`">
          <img src="@/assets/teams-logos/LAC.png"/>
          <img src="@/assets/teams-logos/GSW.png"/>
        </router-link>
      </div>

      <div class="logos-container">
        <router-link :to="`/games/uta-hou`">
          <img src="@/assets/teams-logos/UTA.png"/>
          <img src="@/assets/teams-logos/HOU.png"/>
        </router-link>
      </div>

      <div class="logos-container">
        <router-link :to="`/games/por-okc`">
          <img src="@/assets/teams-logos/POR.png"/>
          <img src="@/assets/teams-logos/OKC.png"/>
        </router-link>
      </div>

      <div class="logos-container">
        <router-link :to="`/games/den-sas`">
          <img src="@/assets/teams-logos/DEN.png"/>
          <img src="@/assets/teams-logos/SAS.png"/>
        </router-link>
      </div>

      <div class="logos-container">
        <router-link :to="`/games/mil-det`">
          <img src="@/assets/teams-logos/MIL.png"/>
          <img src="@/assets/teams-logos/DET.png"/>
        </router-link>
      </div>

      <div class="logos-container">
        <router-link :to="`/games/bos-ind`">
          <img src="@/assets/teams-logos/BOS.png"/>
          <img src="@/assets/teams-logos/IND.png"/>
        </router-link>
      </div>

      <div class="logos-container">
        <router-link :to="`/games/phi-bkn`">
          <img src="@/assets/teams-logos/PHI.png"/>
          <img src="@/assets/teams-logos/BKN.png"/>
        </router-link>
      </div>

      <div class="logos-container">
        <router-link :to="`/games/tor-orl`">
          <img src="@/assets/teams-logos/TOR.png"/>
          <img src="@/assets/teams-logos/ORL.png"/>
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
