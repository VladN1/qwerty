<template>
  <div class="informer-container">
    <temp v-bind:real="weather.temp_real" v-bind:feel="weather.temp_feel" />
    <flex/>
    <hum v-bind:val="hum" />
    <vert/>
    <wind v-bind:val="wind" />
  </div>
</template>
<script>
import temp from './temp.vue';
import hum from './hum.vue';
import wind from './wind.vue';
import flex from './flex.vue';
import vert from './vert.vue';
export default{
  name: 'informer',
  props: ['weather'],
  components: {
    temp, hum, wind, flex, vert
  }
}
</script>
<style>
  .informer-container {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  flex-wrap: wrap;
  width: 400px;
  min-height: 255px;
  padding: 30px;
  background-image: url('/img/forest.png');
  background-size: cover;
  background-position: center center;
  border-radius: 20px;
  box-shadow: 0px 0px 10px 0px rgba(50, 50, 50, 0.75);
}
</style>