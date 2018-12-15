<template>
  <div>
    <l-map ref='myMap' :zoom="14" :center="[1.2877931,103.845996]">
      <l-tile-layer :url="url" :attribution="attribution"></l-tile-layer>
    </l-map>
  </div>
</template>

<script>
import {
  LMap,
  LTileLayer
} from 'vue2-leaflet'
export default {
  name: 'HelloWorld',
  components: {
    LMap,
    LTileLayer
  },
  mounted () {
    this.$nextTick(() => {
      this.map = this.$refs.myMap.mapObject
    })
  },
  data () {
    return {
      map: null,
      zoom: 13,
      url: 'http://{s}.tile.osm.org/{z}/{x}/{y}.png',
      attribution: '&copy; <a href="http://osm.org/copyright">OpenStreetMap</a> contributors'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
