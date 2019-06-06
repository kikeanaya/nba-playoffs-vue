<template>
  <div>
  </div>
</template>

<script>

export default {
  data () {
    return {
      games: []
    }
  },
  mounted () {
    switch (this.$route.params.id) {
      case 'lac-gsw': {
        fetch(`https://www.balldontlie.io/api/v1/games?team_ids[]=13&start_date=2019-04-13&end_date=2019-04-26`)
          .then(res => res.json())
          .then(myJson => { this.games = myJson.data })
        break
      }
      case 'uta-hou': {
        fetch(`https://www.balldontlie.io/api/v1/games?team_ids[]=29&start_date=2019-04-14&end_date=2019-04-24`)
          .then(res => res.json())
          .then(myJson => { this.games = myJson.data })
        break
      }
      case 'por-okc': {
        fetch(`https://www.balldontlie.io/api/v1/games?team_ids[]=25&start_date=2019-04-14&end_date=2019-04-24`)
          .then(res => res.json())
          .then(myJson => { this.games = myJson.data })
        break
      }
      case 'den-sas': {
        fetch(`https://www.balldontlie.io/api/v1/games?team_ids[]=27&start_date=2019-04-13&end_date=2019-04-27`)
          .then(res => res.json())
          .then(myJson => { this.games = myJson.data })
        break
      }
      case 'mil-det': {
        fetch(`https://www.balldontlie.io/api/v1/games?team_ids[]=17&start_date=2019-04-14&end_date=2019-04-22`)
          .then(res => res.json())
          .then(myJson => { this.games = myJson.data })
        break
      }
      case 'bos-ind': {
        fetch(`https://www.balldontlie.io/api/v1/games?team_ids[]=2&start_date=2019-04-14&end_date=2019-04-21`)
          .then(res => res.json())
          .then(myJson => { this.games = myJson.data })
        break
      }
      case 'phi-bkn': {
        fetch(`https://www.balldontlie.io/api/v1/games?team_ids[]=3&start_date=2019-04-13&end_date=2019-04-23`)
          .then(res => res.json())
          .then(myJson => { this.games = myJson.data })
        break
      }
      case 'tor-orl': {
        fetch(`https://www.balldontlie.io/api/v1/games?team_ids[]=28&start_date=2019-04-13&end_date=2019-04-23`)
          .then(res => res.json())
          .then(myJson => { this.games = myJson.data })
        break
      }
    }
  }
}
</script>
