<template>
  <div class="relative z-0 w-full h-[80vh]">
    <div id="mapContainer" class="h-full"></div>
  </div>
</template>

<script>
import { ref, reactive, onMounted, watch } from "vue";
import "leaflet/dist/leaflet.css";
import L from "leaflet";

export default {
  name: "map-component",
  setup() {
    const mainMap = ref(null);
    const currCenter = ref(null);
    const initLocation = reactive({
      lat: 0,
      lon: 39,
    });
    const ipLocation = ref(null);

    const createMapLayer = () => {
      mainMap.value = L.map("mapContainer").setView([40, 0], 5);

      L.tileLayer("https://tile.openstreetmap.org/{z}/{x}/{y}.png", {
        attribution:
          '&copy; <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a>',
      }).addTo(mainMap.value);
      setmarker();
    };

    const setmarker = () => {
      return L.marker([40, 0]).addTo(mainMap.value);
    };

    onMounted(() => {
      createMapLayer();
    });

    return {};
  },
};
</script>

<style lang="scss" scoped></style>
