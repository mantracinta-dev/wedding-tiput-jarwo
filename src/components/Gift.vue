<template>
  <div class="text-center m-auto py-10">
    <v-container>
      <!-- <v-icon x-large color="pink lighten-2" class="mb-2"> mdi-gift-outline </v-icon>
      <p>Kirim Hadiah</p>
      <p class="text-sm">Doa Restu Anda merupakan karunia yang sangat berarti bagi kami. Namun jika memberi adalah ungkapan tanda kasih Anda, Anda dapat memberi kado secara cashless.</p>
      <div class="mb-5">
        <v-btn x-small color="info" rounded class="py-4">
          <v-icon dark small class="mr-1"> mdi-gift </v-icon>
          Amplop Digital
        </v-btn>
      </div> -->
      <p class="text-sm">Atas kehadiran dan do’a restu dari bapak/ibu/saudara/I sekalian, kami mengucapkan Terima Kasih.</p>
      <p class="font__cursive color__yellow text-2xl">Wassalamualaikum Wr. Wb.</p>
      <div class="relative flex items-center justify-center h-36">
        <div class="absolute left-0 right-0 -top-18 text-center">
          <v-img class="m-auto" lazy-src="../assets/img/linecentral.png" max-width="200" src="../assets/img/linecentral.png" alt="img-line" />
        </div>
        <p data-aos="zoom-in" data-aos-duration="1500" class="font__title font-bold text-5xl color__pink">TJ</p>
      </div>
      <p class="text-sm">
        Kami yang berbahagia <br />
        <span class="font__cursive color__yellow text-2xl pt-10"> {{ women }} & {{ man }} </span>
      </p>
    </v-container>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped></style>
