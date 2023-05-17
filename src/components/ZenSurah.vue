<template>
    <div class="center surah" :start="false">
        <div class="typed">
            Dan di antara tanda-tanda (kebesaran)-Nya ialah Dia menciptakan pasangan-pasangan untukmu dari jenismu sendiri, agar kamu cenderung dan merasa tenteram kepadanya, dan Dia menjadikan di antaramu rasa kasih dan sayang. Sungguh, pada yang demikian itu benar-benar terdapat tanda-tanda (kebesaran Allah) bagi kaum yang berpikir.
        </div>
        <div class="css-typing"></div>
        <p class="hide"> ( QS. Ar-Rum Ayat 21 )</p>  
    </div>
</template>

<script>
export default {

    props: {
        start: {type: Boolean, default: false},
    },
    watch: {
        start:  function(newVal, oldVal) { // watch it
          console.log('Prop changed: ', newVal, ' | was: ', oldVal)
        }
    }
}

</script>

<style scoped>
    .surah{
        color: violet;
        height: var(--cover-height);
        text-align: center;
        font-size: 1.8em;
        width: 100%;
    }
    .typed {
        color: violet;

    }
</style>
