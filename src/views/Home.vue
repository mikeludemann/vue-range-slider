<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <rangeSlider min="1" max="1000" step="10" name="test" id="test1"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue';
import rangeSlider from '@/components/range-slider.vue';

export default {
  name: 'Home',
  components: {
    HelloWorld,
    rangeSlider
  }
}
</script>
