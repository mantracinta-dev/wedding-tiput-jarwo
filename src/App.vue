<template>
  <v-app>
    <v-main class="pb-15 bg-greeting">
      <card-greeting :dialog="dialog" :guest="guest" @open="btnOpen" />
      <floating-button :audio="audio" @music="play(audio)" @top="btnTop" />
      <router-view />
    </v-main>
    <!-- <Preloader :loader="load" /> -->
  </v-app>
</template>

<script>
// import Preloader from "../src/components/MyPreloader.vue";
import CardGreeting from './components/CardGreeting.vue'
import FloatingButton from './components/FloatingButton.vue'

export default {
  name: 'App',
  components: {
    // Preloader,
    CardGreeting,
    FloatingButton
  },

  data: () => ({
    dialog: true,
    load: true,
    guest: '',
    audio: {
      id: 'music-love',
      name: 'kau-ditakdirkan-untukku',
      file: new Audio(require('/public/Gending-Temanten-Adat-Jawa-kebo-giro.mp3')),
      isPlaying: false
    }
  }),

  created() {
    const check = sessionStorage.getItem('guest')
    if (check) {
      this.guest = check
      this.dialog = false
    } else {
      this.guest = this.$route.query.to
    }
  },

  methods: {
    btnTop() {
      window.scrollTo(0, 0)
    },
    btnOpen() {
      this.dialog = false
      this.play(this.audio)
      // sessionStorage.setItem("guest", this.guest);
    },
    play(audio) {
      audio.isPlaying = !audio.isPlaying
      if (audio.isPlaying != true) {
        this.pause(audio)
      } else {
        audio.file.play()
      }
    },
    pause(audio) {
      audio.isPlaying = false
      audio.file.pause()
    }
  }
}
</script>
