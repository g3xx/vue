<script setup >

import Boot from './components/Boot.vue'

import { onMounted } from "vue";
import AOS from "aos";

onMounted(() => {
    AOS.init({
      offset: 200,
      duration: 1000,
      easing: 'ease-in-sine',
      delay: 150,
      once: false,
    });
})


</script>

<template>
    <Boot/>
</template>



