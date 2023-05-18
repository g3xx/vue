<script setup >

import Boot from './components/Boot.vue'

import { onMounted } from "vue";
import AOS from "aos";

onMounted(() => {
    AOS.init({
      offset: 200,
      duration: 800,
      easing: 'ease-in-sine',
      delay: 100,
      once: false,
      useClassNames: true,
    });
})


</script>

<template>
    <Boot/>
</template>



