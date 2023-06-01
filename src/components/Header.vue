<template>
  <div class="min-h-screen text-center m-auto">
    <v-container>
      <v-row>
        <v-col cols="12">
          <p class="text-uppercase p-2 mb-0 tracking-widest">WALIMATUL 'URS</p>
          <v-img
            class="m-auto"
            lazy-src="../assets/img/rumah-gadang.png"
            max-width="100"
            src="../assets/img/rumah-gadang.png"
            alt="img-rumah-gadang"
          />
        </v-col>
        <v-col cols="12" class="py-5">
          <h1
            class="font__cursive text-5xl pink--text font-font-semibold"
            data-aos="fade-up"
            data-aos-duration="1500"
          >
            Aufa & Ridho
          </h1>
          <div class="my-5">
            <v-img
              class="m-auto"
              lazy-src="../assets/img/line.png"
              max-width="180"
              src="../assets/img/line.png"
              alt="img-line"
            />
          </div>
          <div class="my-2" data-aos="zoom-in" data-aos-duration="1500">
            <v-img
              class="m-auto"
              lazy-src="../assets/img/lovechar.png"
              max-width="100%"
              src="../assets/img/lovechar.png"
              alt="img-love-couple"
            />
          </div>
          <div
            data-aos="fade-up"
            data-aos-duration="1500"
            data-aos-anchor-placement="top-bottom"
          >
            <p class="font-bold text-lg tracking-widest font__title">
              Minggu, 12 Juni 2022 <br />
              Pekanbaru
            </p>
            <p id="time" />
          </div>
          <div class="my-5">
            <v-img
              class="m-auto"
              lazy-src="../assets/img/line.png"
              max-width="180"
              src="../assets/img/line.png"
              alt="img-line"
            />
          </div>
        </v-col>
        <v-col
          cols="12"
          class="pb-5"
          data-aos="zoom-in"
          data-aos-duration="1500"
        >
          <h1 class="font__cursive text-2xl font-semibold color__purple">
            QS. Ar-Rum Ayat 21
          </h1>
          <p class="text-sm">
            Dan di antara tanda-tanda (kebesaran)-Nya ialah Dia menciptakan
            pasangan-pasangan untukmu dari jenismu sendiri, agar kamu cenderung
            dan merasa tenteram kepadanya, dan Dia menjadikan di antaramu rasa
            kasih dan sayang. Sungguh, pada yang demikian itu benar-benar
            terdapat tanda-tanda (kebesaran Allah) bagi kaum yang berpikir.
          </p>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  mounted() {
    // Set the date we're counting down to
    var countDownDate = new Date("Jun 12, 2022 08:00:00").getTime();

    // Update the count down every 1 second
    var countdownfunction = setInterval(function () {
      // Get todays date and time
      var now = new Date().getTime();

      // Find the distance between now an the count down date
      var distance = countDownDate - now;

      // Time calculations for days, hours, minutes and seconds
      var days = Math.floor(distance / (1000 * 60 * 60 * 24));
      var hours = Math.floor(
        (distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60)
      );
      var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
      var seconds = Math.floor((distance % (1000 * 60)) / 1000);

      // Output the result in an element with id="demo"
      document.getElementById("time").innerHTML =
        days +
        " Hari " +
        hours +
        " Jam " +
        minutes +
        " Min " +
        seconds +
        " Detik ";

      // If the count down is over, write some text
      if (distance < 0) {
        clearInterval(countdownfunction);
        document.getElementById("time").innerHTML = "Sudah Halal";
      }
    }, 1000);
  },
};
</script>

<style lang="scss" scoped>
</style>