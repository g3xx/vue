<template>
    <div class="center surah" v-if="this.$parent.start">
        <div class="typed" ref="surah">
            Dan di antara tanda-tanda (kebesaran)-Nya ialah Dia menciptakan pasangan-pasangan untukmu dari jenismu sendiri, agar kamu cenderung dan merasa tenteram kepadanya, dan Dia menjadikan di antaramu rasa kasih dan sayang. Sungguh, pada yang demikian itu benar-benar terdapat tanda-tanda (kebesaran Allah) bagi kaum yang berpikir.
        </div>
        <div ref="surahx"></div>
        <p class="hide" ref="qs"> ( QS. Ar-Rum Ayat 21 )</p>  
    </div>
</template>

<script>
export default {

    props: {
        start: {type: Boolean, default: false},
    },

    methods: {
        typing(){
            const text = this.$refs.surah.innerText
            const span = '<span>' + text.split('').join('</span><span>') + '</span>';
            this.$refs.surahx.insertAdjacentHTML('afterbegin', span);
            const spans = document.querySelectorAll("span")
            const count = spans.length;
            setTimeout(() => {
                spans.forEach((el, i) => {
                    setTimeout(() => {
                        el.classList.add("typex")
                    }, 15*i)
                })
                setTimeout(() => {
                    this.$refs.qs.classList.remove("hide")
                    this.$refs.qs.classList.add("show")
                }, 15*count+20)    
            }, 100)
        }
    },
    mounted() {
        this.$watch(
            "$parent.start", () => { 
                this.$nextTick(()=>{ this.typing() })
            }
        );
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
    ::v-deep span, .typed, .hide {
        display: none;

    }
    .show {
        animation: fadeInFromNone 2.5s ease-out;
    }
    p {
        margin-top: 2em;
    }
    ::v-deep .typex {
        display: inline !important;
        font-family: var(--fm-norican);
        -webkit-animation: fadeInFromNone 0.5s ease-out;
        -moz-animation: fadeInFromNone 0.5s ease-out;
        -o-animation: fadeInFromNone 0.5s ease-out;
        animation: fadeInFromNone 0.5s ease-out;
    }

    @keyframes fadeInFromNone {
        0% { display: none; opacity: 0;}
        1% { display: block; mopacity: 0; }
        100% { display: block; opacity: 1; }
    }
</style>
