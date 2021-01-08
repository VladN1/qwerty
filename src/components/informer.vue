<template>
  <div class="informer-container">
    <temp/>
    <flex/>
    <hum/>
    <vert/>
    <wind/>
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