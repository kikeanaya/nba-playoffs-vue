<template>
    <div class="main-container">
      <div class="conferences-titles">
        <h2>WEST</h2>
        <h2>EAST</h2>
      </div>

      <div class="stages">
        <h3>ROUND 1</h3>
        <h3>SEMIFINALS</h3>
        <h3>CONFERENCE FINALS</h3>
        <h2>FINALS</h2>
        <h3>CONFERENCE FINALS</h3>
        <h3>SEMIFINALS</h3>
        <h3>ROUND 1</h3>
      </div>

      <div class="games-container">
      <div class="quarter-finals">
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
      </div>
    <div class="quarter-finals">
      <div class="logos-container">
        <router-link :to="`/games/gsw-hou`">
          <img src="@/assets/teams-logos/GSW.png"/>
          <img src="@/assets/teams-logos/HOU.png"/>
        </router-link>
      </div>

      <div class="logos-container">
        <router-link :to="`/games/por-dev`">
          <img src="@/assets/teams-logos/POR.png"/>
          <img src="@/assets/teams-logos/DEN.png"/>
        </router-link>
      </div>
    </div>
     <div class="quarter-finals">
     
      <div class="logos-container">
        <router-link :to="`/games/gsw-por`">
          <img src="@/assets/teams-logos/GSW.png"/>
          <img src="@/assets/teams-logos/POR.png"/>
        </router-link>
      </div>
    </div>
    <div class="quarter-finals">
      <div class="logos-container">
        <router-link :to="`/games/gsw-tor`">
          <img src="@/assets/teams-logos/GSW.png"/>
          <img src="@/assets/teams-logos/TOR.png"/>
        </router-link>
      </div>
    </div>

    <div class="quarter-finals">
      <div class="logos-container">
        <router-link :to="`/games/mil-tor`">
          <img src="@/assets/teams-logos/MIL.png"/>
          <img src="@/assets/teams-logos/TOR.png"/>
        </router-link>
      </div>
      
    </div>


    <div class="quarter-finals">
      <div class="logos-container">
        <router-link :to="`/games/mil-bos`">
          <img src="@/assets/teams-logos/MIL.png"/>
          <img src="@/assets/teams-logos/BOS.png"/>
        </router-link>
      </div>

      <div class="logos-container">
        <router-link :to="`/games/phi-tor`">
          <img src="@/assets/teams-logos/PHI.png"/>
          <img src="@/assets/teams-logos/TOR.png"/>
        </router-link>
      </div>
    </div>

    <div class="quarter-finals">
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
