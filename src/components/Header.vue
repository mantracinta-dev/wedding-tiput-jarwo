<template>
  <div class="min-h-screen text-center m-auto">
    <v-container>
      <v-row>
        <v-col cols="12">
          <div class="h-screen bg-cover">
            <div class="card-header" data-aos="fade-up" data-aos-duration="1500" data-aos-anchor-placement="top-bottom">
              <v-img class="m-auto" lazy-src="../assets/img/ornament.png" max-width="180" src="../assets/img/ornament.png" alt="img-ornament" />
              <h1 class="font__cursive text-capitalize my-2 lg:text-6xl text-5xl text-white my-5">{{ women }} & {{ man }}</h1>
              <p class="text-sm tracking-widest font__title text-white">
                Minggu, 12 Juni 2022 <br />
                Bandung
              </p>
              <p class="text-white" id="time" />
            </div>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  mounted() {
    // Set the date we're counting down to
    var countDownDate = new Date('Jul 09, 2023 08:00:00').getTime()

    // Update the count down every 1 second
    var countdownfunction = setInterval(function () {
      // Get todays date and time
      var now = new Date().getTime()

      // Find the distance between now an the count down date
      var distance = countDownDate - now

      // Time calculations for days, hours, minutes and seconds
      var days = Math.floor(distance / (1000 * 60 * 60 * 24))
      var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60))
      var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60))
      var seconds = Math.floor((distance % (1000 * 60)) / 1000)

      // Output the result in an element with id="demo"
      document.getElementById('time').innerHTML = days + ' Hari ' + hours + ' Jam ' + minutes + ' Min ' + seconds + ' Detik '

      // If the count down is over, write some text
      if (distance < 0) {
        clearInterval(countdownfunction)
        document.getElementById('time').innerHTML = 'Sudah Halal'
      }
    }, 1000)
  }
}
</script>

<style lang="scss" scoped></style>
