<template>
        <div v-show="this.$parent.start">
            <ZenWrap>
            <div class="box">
                <div data-aos="fade-up">
                    <h2>بِسْمِ اللّهِ الرَّحْمَنِ الرَّحِيْمِ </h2>
                </div>
            </div>
            </ZenWrap>
            <ZenWrap>
                <div class="box">The Wedding of</div>
                <div class="box">The Wedding of</div>
            </ZenWrap>
            <ZenWrap>
                <div class="box">The Wedding of</div>
                <div class="box">The Wedding of</div>
            </ZenWrap>
            <ZenWrap>
                <div class="box">The Wedding of</div>
                <div class="box">The Wedding of</div>
            </ZenWrap>
            <ZenWrap>
                <div class="box">The Wedding of</div>
                <div class="box">The Wedding of</div>
            </ZenWrap>
            <ZenWrap>
                <div class="box">The Wedding of</div>
                <div class="box">The Wedding of</div>
            </ZenWrap>
        </div>


</template>

<script>

import ZenWrap from './ZenWrap.vue'

export default {

    components: { ZenWrap },
  
}
</script>


<style scoped>
    h2 {
        margin: 20px 0;
        font-size: 2em;
    }

    .box {
        margin: 20px 0;
    }
</style>