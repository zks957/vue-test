<script setup lang="ts">
import Slick from 'vue-slick';
import { ref } from 'vue';
// Events listeners
const handleAfterChange = (event:any, slick:any, currentSlide:any) => {
    console.log('handleAfterChange', event, slick, currentSlide);
};

const slickOptions = ref({
                            slidesToShow: 3,
                            // Any other options that can be got from plugin documentation
                        }) 
</script>

<template>
    <slick
      ref="slick"
      :options="slickOptions"
      @afterChange="handleAfterChange">
      <div class="item"></div>
      <div class="item"></div>
      <div class="item"></div>
      <div class="item"></div>
    </slick>
</template>

<style scoped>
.item {
  height: 100px;
  width: 500px;
  background-color: antiquewhite;
  border: 1px solid #fff;
}
</style>
