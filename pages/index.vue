<template>
  <v-row>
<!--
    <div class="tradingview-widget-container">
  
 <script type="text/javascript" src="https://s3.tradingview.com/external-embedding/embed-widget-ticker-tape.js" async>
 {
 "symbols": [
   {
     "proName": "FOREXCOM:SPXUSD",
     "title": "S&P 500"
   },
   {
     "proName": "FOREXCOM:NSXUSD",
     "title": "US 100"
   },
   {
     "proName": "FX_IDC:EURUSD",
     "title": "EUR/USD"
   },
   {
     "proName": "BITSTAMP:BTCUSD",
     "title": "Bitcoin"
   },
   {
     "proName": "BITSTAMP:ETHUSD",
     "title": "Ethereum"
   }
 ],
 "showSymbolLogo": true,
 "colorTheme": "dark",
 "isTransparent": false,
 "displayMode": "adaptive",
 "locale": "en"
}
 </script>
</div>
TradingView Widget END -->

    <NavBar />

    <!-- Start title with typewritter  -->
    <v-row class="mt-16">
      <v-col col="12" md="2"></v-col>

      <v-col class="initTextWrapper" col="12" md="8" align="center">
        <h1 id="greenWord" class="mainTitle">EXPLORE</h1>
        <h1 class="mainTitle">
          THE BEST INFO PLACE FOR BEGGINERS AND CRIPTOLOVERS!
        </h1>
      </v-col>

      <v-col col="12" md="2"></v-col>
    </v-row>


    <!-- First icons  -->

    <v-row>
      <v-col col="12" md="1"></v-col>

      <v-col
        class="iconsWrapper mt-10"
        col="12"
        md="10"
        justify-content="center"
      >
        <div class="iconContentWrapper">
          <v-icon
            size="40"
            color="teal"
            class="iconSelf mr-2"
          >mdi-book-edit</v-icon>
          <div class="textIconWrapper">
          <h3>100+</h3>
          <h5>Articles</h5>
        </div>
      </div>

        <div class="iconContentWrapper">
          <v-icon
            size="40"
            color="teal"
            class="iconSelf mr-2"
          >mdi-newspaper</v-icon>
          <div class="textIconWrapper">
          <h3>10+</h3>
          <h5>Notices/day</h5>
        </div>
      </div>

        <div class="iconContentWrapper">
          <v-icon
            size="40"
            color="teal"
            class="iconSelf mr-2"
          >mdi-earth</v-icon>
          <div class="textIconWrapper">
          <h3>1000+</h3>
          <h5>Views</h5>
        </div>
      </div>

      <div id="resumeTextWrapper" class="pl-2">
          <h4>Find notices, articles, graphics, quickly, with a plain language. The best way to learn, and gain money.</h4>
         </div>


      </v-col>

      <v-col col="12" md="1"></v-col>
    </v-row>




    <!-- Caroulsel  -->

    <v-carousel
      class="mt-16"
      cycle
      height="40rem"
      hide-delimiter-background
      show-arrows-on-hover
    >
      <v-carousel-item v-for="(slide, i) in slides" :key="i">
        <v-row class="fill-height" align="end" justify="center">
          <img :src="colors[i]" width="100%" />

          <div class="text-h2 mb-15">{{ slide }} Slide</div>
        </v-row>
      </v-carousel-item>
    </v-carousel>
  </v-row>
</template>

<style>

  /*Start title with typewritter*/

  .initTextWrapper .mainTitle {
    font-size: 32pt;
    font-family: 'Roboto', sans-serif !important; /*Não tá indo essa porra*/
  }

  #greenWord {
    color: teal;
  }


  /*First Icons */

  .iconsWrapper {
    display: flex;
    justify-content: space-between;
  }

  .iconsWrapper .iconContentWrapper {
    display: flex;
    align-items: center;
  }

  .iconsWrapper .iconContentWrapper .iconSelf {
    background-color: #fff;
    padding: .3rem;
    border-radius: 10px;
  }

  .iconsWrapper #resumeTextWrapper {
    width: 30%;
    border-left: solid 2px teal;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  /*Caroulsel*/

  .text-h2 {
    position: absolute;

    background: rgba(255, 255, 255, 0) !important;
    box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1) !important;
    backdrop-filter: blur(3.4px) !important;
    border: none !important;
  }



</style>


<script>
import NavBar from '~/components/navBar.vue'
export default {
  name: 'IndexPage',
  data() {
    return {
      colors: [
        'img/imgtest.jpg',
        'warning',
        'pink darken-2',
        'red lighten-1',
        'deep-purple accent-4',
      ],
      slides: [
        'Os touros Cardano perdem o fôlego após o hard fork Vasil: Queda de preço de 40% ADA.',
        'Second',
        'Third',
        'Fourth',
        'Fifth',
      ],
    }
  },
  components: { NavBar },
  /*
  methods: {
    typeWriter () {
      const elementTitle1 = document.querySelector('#greenWord')
      const elementTitle2 = document.querySelector('.mainTitle')

      const arrGreenWord = elementTitle1.innerHTML.split('');
      const arrPhrase = elementTitle2.innerHTML.split('');
      elementTitle1.innerHTML = '';
      elementTitle2.innerHTML = '';
      elementTitle1.style.opacity = '1';
      elementTitle2.style.opacity = '1';

      arrGreenWord.forEach((element, ind) => {
          setTimeout(() => elementTitle1.innerHTML += element, 75 * ind);
      });

      setTimeout(() => {
        arrPhrase.forEach((element, ind) => {
          setTimeout(() => elementTitle2.innerHTML += element  , 75 * ind);
      }) 
      }, 1300);
  }*/

}
</script>
