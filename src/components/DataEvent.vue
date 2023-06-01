<template>
  <div id="event" class="min-h-screen text-center m-auto bg-white py-10 rounded-3xl bg-card">
    <div class="mb-10">
      <v-img class="m-auto" lazy-src="../assets/img/linetop.png" max-width="100" src="../assets/img/linetop.png" alt="img-line" />
    </div>
    <h1 class="text-3xl font__cursive font-semibold color__pink">Akad Nikah</h1>
    <p class="font__title text-lg font-semibold uppercase">Sunday</p>
    <div class="relative flex items-center justify-center h-36">
      <div class="absolute left-0 right-0 -top-18 text-center">
        <v-img class="m-auto" lazy-src="../assets/img/linecentral.png" max-width="200" src="../assets/img/linecentral.png" alt="img-line" />
      </div>
      <p data-aos="zoom-in" data-aos-duration="1500" class="font__title font-bold text-5xl color__purple">09</p>
    </div>
    <p>
      <span class="font__title text-lg font-semibold uppercase"> July 2023 </span>
      <br />
      Pukul <b>08:00 Wib</b> s/d Selesai
    </p>
    <div>
      <v-img class="m-auto" lazy-src="../assets/img/rumah-gadang.png" max-width="100" src="../assets/img/rumah-gadang.png" alt="img-rumah-gadang" />
      <p>
        <span class="font__cursive text-xl color__pink font-semibold">Lokasi Acara</span>
        <br />
        <b>The White Clover</b> <br />
        <span class="text-sm"> Jl. Dr. Cipto No.24, Pasir Kaliki, Kec. Cicendo, Kota Bandung </span>
      </p>
      <v-btn x-small color="info" rounded class="py-4" @click="openMap()">
        <v-icon dark small class="mr-1"> mdi-map-marker-outline </v-icon>
        Lihat Lokasi
      </v-btn>
    </div>
    <div class="mt-10">
      <v-img class="m-auto rotate-180" lazy-src="../assets/img/linetop.png" max-width="100" src="../assets/img/linetop.png" alt="img-line" />
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    openMap() {
      window.open('https://goo.gl/maps/hB9KeWNLQFrtHfZD6?coh=178571&entry=tt', '_blank')
    }
  }
}
</script>

<style lang="scss" scoped></style>
