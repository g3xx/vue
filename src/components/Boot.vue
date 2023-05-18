<script>

import ZenIntro from './ZenIntro.vue'
import ZenSurah from './ZenSurah.vue'

export default {

    components: { ZenIntro, ZenSurah },
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

</template>



