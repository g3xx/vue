<script>

import ZenIntro from './ZenIntro.vue'
import ZenSurah from './ZenSurah.vue'
import ZenProfile from './ZenProfile.vue'

export default {

    components: { ZenIntro, ZenSurah, ZenProfile },
    data() {
        return {
            start : false
        }
    }

}

</script>

<template>

    <ZenIntro/>
    <zenSurah/>
    <ZenProfile/>

</template>



