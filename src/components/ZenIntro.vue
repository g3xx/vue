<template>
    <div class="intro center">
      <div class="filter"></div>
      <p data-aos="fade-down">The Wedding of</p>
        <div data-aos="zoom-in" data-aos-delay="500">
          <h1>Danela &amp; Daffin </h1>
        </div>
        <p data-aos="fade-up">18 Desember 2022</p>
        <button data-aos="fade-up" data-aos-delay="750" @click="hideIntro()">Open Invitation</button>
    </div>
</template>

<script>

  export default {
    data(){
      return {
        img : `url(${this.image})`
      }
    },

    props: {
      image: { type: String, default: "https://source.unsplash.com/2UuZFFefnRc" }
    },
    methods: {
      hideIntro() {
        const el = document.querySelector('.intro');
        el.setAttribute("data-aos", "fade-up");
        setTimeout(() => { document.querySelector(".intro").remove() }, 1000)
        console.log("work")
        const ex = document.querySelector('.surah');
        ex.setAttribute("start", true);
      }
    },

   
  }

</script>

<style scoped>
  .intro {
    width: 100%;
    height: var(--cover-height);
    text-align: center;
    position: fixed;
    top: 0;
    left: 0;
    z-index: 9999;
    overflow: hidden;
    opacity: 1;
    transition: all 2.2s;
    background-image: v-bind("img");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
  }

  p {
    font: 1em sans-serif;
    font-size: calc(var(--f-subtitle) + 2px);
    text-transform: uppercase;
    letter-spacing: 3px;
  }
  h1 {
    font-size: 4em;
    margin: 10px 0;
    
  }
  button {
    margin: 5em 0;
    border-radius: 8px;
    border: 1px solid transparent;
    padding: 1em 1.3em;
    font-size: 1em;
    font-weight: 500;
    font-family: inherit;
    background-color: #1a1a1a;
    cursor: pointer;
    transition: border-color 0.25s;
  }
  button:hover {
    background-color: #2b2525;
  }
  button:focus,
  button:focus-visible {
    outline: 4px auto -webkit-focus-ring-color;
  }
  .filter {
    position:absolute;
    width:100%;
    height:100%;
    background: rgba(0, 0, 0, 0.75);
  }
</style>
