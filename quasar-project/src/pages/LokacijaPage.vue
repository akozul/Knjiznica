<template>
  <div id="map" style="height: 500px;"></div>
</template>

<script setup>
import { ref, onMounted } from 'vue';
import * as L from 'leaflet';
import 'leaflet/dist/leaflet.css';

const initialMap = ref(null)

onMounted(() => {
  // Inicijalizacija mape
  initialMap.value = L.map('map').setView([45.3312, 14.4322], 13)

  // Postavljanje tile layera (OpenStreetMap)
  L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
    maxZoom: 19,
    attribution: '&copy; <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a>'
  }).addTo(initialMap.value)
})
</script>

<style>
/* Opcionalno: osigurava da mapa zauzima cijeli raspoloživi prostor */
#map {
  width: 100%;
  height: 500px;
}
</style>
