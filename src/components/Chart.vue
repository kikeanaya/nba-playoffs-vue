<script>
import { Line } from 'vue-chartjs'

export default ({
  extends: Line,

  props: {
    games: Array
  },  
  data () {
    return {
      gradient: null,
      gradient2: null,
      teamOneScores: [],
      teamTwoScores: [],
      teamOneName: '',
      teamTwoName: '',
      labels: []
    }
  },
  mounted () {
    this.gradient = this.$refs.canvas.getContext('2d').createLinearGradient(0, 0, 0, 450)
    this.gradient2 = this.$refs.canvas.getContext('2d').createLinearGradient(0, 0, 0, 450)

    this.gradient.addColorStop(0, 'rgba(255, 0,0, 0.5)')
    this.gradient.addColorStop(0.5, 'rgba(255, 0, 0, 0.25)')
    this.gradient.addColorStop(1, 'rgba(255, 0, 0, 0)')

    this.gradient2.addColorStop(0, 'rgba(0, 231, 255, 0.9)')
    this.gradient2.addColorStop(0.5, 'rgba(0, 231, 255, 0.25)')
    this.gradient2.addColorStop(1, 'rgba(0, 231, 255, 0)')

    this.teamOneName = this.games[0].home_team.abbreviation
    this.teamTwoName = this.games[0].visitor_team.abbreviation

    for(let i = 0; i<this.games.length; i++){
      this.labels.push(`Game ${i+1}`)
      if(this.games[i].home_team.abbreviation === this.teamOneName){
        this.teamOneScores.push(this.games[i].home_team_score)
        this.teamTwoScores.push(this.games[i].visitor_team_score)
      } else{
        this.teamOneScores.push(this.games[i].visitor_team_score)
        this.teamTwoScores.push(this.games[i].home_team_score)
      }
    }  

    this.renderChart({
      labels: this.labels, // partidos
      datasets: [
        {
          label: this.teamOneName, // equipo
          borderColor: '#FC2525',
          pointBackgroundColor: 'white',
          borderWidth: 1,
          pointBorderColor: 'white',
          backgroundColor: this.gradient,
          data: this.teamOneScores // puntos
        }, {
          label: this.teamTwoName,
          borderColor: '#05CBE1',
          pointBackgroundColor: 'white',
          pointBorderColor: 'white',
          borderWidth: 1,
          backgroundColor: this.gradient2,
          data: this.teamTwoScores
        }
      ]
    }, { responsive: true, maintainAspectRatio: false })
  }
})

</script>
