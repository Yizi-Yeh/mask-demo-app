
<template>
  <div id="app">
    <!-- 側欄元件 -->
    <aside-menu />
    <maskMap />
    <light-box />
  </div>
</template>
<script>
import { mapActions } from 'vuex'
import asideMenu from './components/asideMenu.vue'
import lightBox from './components/lightbox.vue'
import maskMap from './components/maskMap.vue'
export default {
  name: 'App',
  components: {
    asideMenu,
    lightBox,
    maskMap

  },
  methods: {
    ...mapActions(['fetchLocations', 'fetchPharmacies'])
  },
  mounted () {
    this.fetchLocations()
    this.fetchPharmacies()
  }
}
</script>

<style lang="scss" src="./style.scss"></style>
