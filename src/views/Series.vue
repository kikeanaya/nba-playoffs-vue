<template>
  <div>
    <div class="logos-in-detailed">
      <img v-if="games.length > 0" :src="require(`../assets/teams-logos/${games[0].home_team.abbreviation}.png`)"/>
      <img v-if="games.length > 0" :src="require(`../assets/teams-logos/${games[0].visitor_team.abbreviation}.png`)"/>
    </div>
    
    <ul class="scores-list">
      <li class="individual-scores" v-for="(game, index) in games" :key="`game-${index}`">
        Game {{index +1}}:
        {{game.home_team.abbreviation}}
        {{game.home_team_score}}
        {{game.visitor_team.abbreviation}}
        {{game.visitor_team_score}}
      </li>
    </ul>
    <Chart
      v-if="games.length > 0"
      :games="games"
    />
  </div>
</template>

<script>
import Chart from '@/components/Chart.vue'

export default {
  data () {
    return {
      games: [],
      loaded: false
    }
  },
  components: {
    Chart
  },
  mounted () {
    this.loaded = false

    switch (this.$route.params.id) {
      case 'lac-gsw': {
        fetch(`https://www.balldontlie.io/api/v1/games?team_ids[]=13&start_date=2019-04-13&end_date=2019-04-26`)
          .then(res => res.json())
          .then(myJson => { this.games = myJson.data })
          .then(this.loaded = true)
        break
      }
      case 'uta-hou': {
        fetch(`https://www.balldontlie.io/api/v1/games?team_ids[]=29&start_date=2019-04-14&end_date=2019-04-24`)
          .then(res => res.json())
          .then(myJson => { this.games = myJson.data })
          .then(this.loaded = true)
        break
      }
      case 'por-okc': {
        fetch(`https://www.balldontlie.io/api/v1/games?team_ids[]=25&start_date=2019-04-14&end_date=2019-04-24`)
          .then(res => res.json())
          .then(myJson => { this.games = myJson.data })
          .then(this.loaded = true)
        break
      }
      case 'den-sas': {
        fetch(`https://www.balldontlie.io/api/v1/games?team_ids[]=27&start_date=2019-04-13&end_date=2019-04-27`)
          .then(res => res.json())
          .then(myJson => { this.games = myJson.data })
          .then(this.loaded = true)
        break
      }
      case 'mil-det': {
        fetch(`https://www.balldontlie.io/api/v1/games?team_ids[]=17&start_date=2019-04-14&end_date=2019-04-22`)
          .then(res => res.json())
          .then(myJson => { this.games = myJson.data })
          .then(this.loaded = true)
        break
      }
      case 'bos-ind': {
        fetch(`https://www.balldontlie.io/api/v1/games?team_ids[]=2&start_date=2019-04-14&end_date=2019-04-21`)
          .then(res => res.json())
          .then(myJson => { this.games = myJson.data })
          .then(this.loaded = true)
        break
      }
      case 'phi-bkn': {
        fetch(`https://www.balldontlie.io/api/v1/games?team_ids[]=3&start_date=2019-04-13&end_date=2019-04-23`)
          .then(res => res.json())
          .then(myJson => { this.games = myJson.data })
          .then(this.loaded = true)
        break
      }
      case 'tor-orl': {
        fetch(`https://www.balldontlie.io/api/v1/games?team_ids[]=28&start_date=2019-04-13&end_date=2019-04-23`)
          .then(res => res.json())
          .then(myJson => { this.games = myJson.data })
          .then(this.loaded = true)
        break
      }
      case 'mil-bos': {
        fetch(`https://www.balldontlie.io/api/v1/games?team_ids[]=2&start_date=2019-04-28&end_date=2019-05-09`)
          .then(res => res.json())
          .then(myJson => { this.games = myJson.data })
          .then(this.loaded = true)
        break
      }
      case 'phi-tor': {
        fetch(`https://www.balldontlie.io/api/v1/games?team_ids[]=28&start_date=2019-04-27&end_date=2019-05-12`)
          .then(res => res.json())
          .then(myJson => { this.games = myJson.data })
          .then(this.loaded = true)
        break
      }
      case 'gsw-hou': {
        fetch(`https://www.balldontlie.io/api/v1/games?team_ids[]=11&start_date=2019-04-28&end_date=2019-05-10`)
          .then(res => res.json())
          .then(myJson => { this.games = myJson.data })
          .then(this.loaded = true)
        break
      }
      case 'por-dev': {
        fetch(`https://www.balldontlie.io/api/v1/games?team_ids[]=9&start_date=2019-04-29&end_date=2019-05-12`)
          .then(res => res.json())
          .then(myJson => { this.games = myJson.data })
          .then(this.loaded = true)
        break
      }
      case 'mil-tor': {
        fetch(`https://www.balldontlie.io/api/v1/games?team_ids[]=28&start_date=2019-05-15&end_date=2019-05-25`)
          .then(res => res.json())
          .then(myJson => { this.games = myJson.data })
          .then(this.loaded = true)
        break
      }
      case 'gsw-por': {
        fetch(`https://www.balldontlie.io/api/v1/games?team_ids[]=25&start_date=2019-05-14&end_date=2019-05-20`)
          .then(res => res.json())
          .then(myJson => { this.games = myJson.data })
          .then(this.loaded = true)
        break
      }
      case 'gsw-tor': {
        fetch(`https://www.balldontlie.io/api/v1/games?team_ids[]=10&start_date=2019-05-30&end_date=2019-06-13`)
          .then(res => res.json())
          .then(myJson => { this.games = myJson.data })
          .then(this.loaded = true)
        break
      }
    }
  }
}
</script>
