<script setup >
import ZenIntro from './components/ZenIntro.vue'
import zenSurah from './components/ZenSurah.vue'

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

    <ZenIntro/>
    <zenSurah/>

</template>



