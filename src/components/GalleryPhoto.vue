<template>
  <div class="min-h-screen text-center m-auto bg-white py-10 rounded-3xl bg-card">
    <CoolLightBox :items="items" :index="imageIndex" @close="imageIndex = null"> </CoolLightBox>

    <div data-aos="fade-up" data-aos-duration="1500">
      <h1 class="font__cursive text-2xl font-semibold color__yellow">Bahagia Kami</h1>
      <p class="text-sm">Mencintai bukan untuk menyamai, tetapi keikhlasan menerima perbedaan.</p>
    </div>

    <v-container>
      <v-row>
        <v-col cols="12">
          <v-img :src="imageSingle" aspect-ratio="1" class="grey lighten-2 rounded">
            <template v-slot:placeholder>
              <v-row class="fill-height ma-0" align="center" justify="center">
                <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
              </v-row>
            </template>
          </v-img>
        </v-col>

        <v-col v-for="(item, index) in items" :key="index" class="d-flex child-flex" cols="4">
          <v-img :src="item.src" aspect-ratio="1" class="grey lighten-2 rounded" @click="chooseImage(item)" @dblclick="imageIndex = index">
            <template v-slot:placeholder>
              <v-row class="fill-height ma-0" align="center" justify="center">
                <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
              </v-row>
            </template>
          </v-img>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import CoolLightBox from 'vue-cool-lightbox'
import 'vue-cool-lightbox/dist/vue-cool-lightbox.min.css'

export default {
  name: 'GalleryPhoto',
  components: {
    CoolLightBox
  },
  data() {
    return {
      imageSingle: require('../assets/img/img (3).jpeg'),
      items: [
        {
          title: 'The Weeding of Tiput & Fajar | #ForAlifeTIme',
          description: 'Undangan by Undangan Epic',
          src: require('../assets/img/img-1.jpg')
        },
        {
          title: 'The Weeding of Tiput & Fajar | #ForAlifeTIme',
          description: 'Undangan by Undangan Epic',
          src: require('../assets/img/img (1).jpg')
        },
        {
          title: 'The Weeding of Tiput & Fajar | #ForAlifeTIme',
          description: 'Undangan by Undangan Epic',
          src: require('../assets/img/img (1).jpeg')
        },
        {
          title: 'The Weeding of Tiput & Fajar | #ForAlifeTIme',
          description: 'Undangan by Undangan Epic',
          src: require('../assets/img/img (2).jpeg')
        },
        {
          title: 'The Weeding of Tiput & Fajar | #ForAlifeTIme',
          description: 'Undangan by Undangan Epic',
          src: require('../assets/img/img (2).jpg')
        },
        {
          title: 'The Weeding of Tiput & Fajar | #ForAlifeTIme',
          description: 'Undangan by Undangan Epic',
          src: require('../assets/img/img (3).jpeg')
        }
      ],
      imageIndex: null
    }
  },
  methods: {
    chooseImage(url) {
      this.imageSingle = url
    }
  }
}
</script>

<style lang="scss" scoped></style>
