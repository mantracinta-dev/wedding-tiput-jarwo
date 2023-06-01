<template>
  <div class="wrapper bg-bg-greeting">
    <Navbar />
    <Header />
    <DataInfo class="mb-2" />
    <DataEvent class="mb-2" />
    <DataEvent2 class="mb-2" />
    <Gift />
    <Footer />
    <Menu />
  </div>
</template>

<script>
import DataEvent from '../components/DataEvent.vue'
import DataEvent2 from '../components/DataEvent2.vue'
import DataInfo from '../components/DataInfo.vue'
import Footer from '../components/Footer.vue'
import Gift from '../components/Gift.vue'
import Header from '../components/Header.vue'
import Menu from '../components/Menu.vue'
import Navbar from '../components/Navbar.vue'
export default {
  name: 'Home',
  components: {
    Header,
    DataInfo,
    Menu,
    Navbar,
    DataEvent,
    DataEvent2,
    Gift,
    Footer
  },
  data() {
    return {}
  },
  methods: {}
}
</script>
