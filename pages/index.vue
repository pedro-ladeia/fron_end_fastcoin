<template>
  <v-row>
    <RodaJequiti />
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
          <v-icon size="40" color="teal" class="iconSelf mr-2"
            >mdi-book-edit</v-icon
          >
          <div class="textIconWrapper">
            <h3>100+</h3>
            <h5>Articles</h5>
          </div>
        </div>

        <div class="iconContentWrapper">
          <v-icon size="40" color="teal" class="iconSelf mr-2"
            >mdi-newspaper</v-icon
          >
          <div class="textIconWrapper">
            <h3>10+</h3>
            <h5>Notices/day</h5>
          </div>
        </div>

        <div class="iconContentWrapper">
          <v-icon size="40" color="teal" class="iconSelf mr-2"
            >mdi-earth</v-icon
          >
          <div class="textIconWrapper">
            <h3>1000+</h3>
            <h5>Views</h5>
          </div>
        </div>

        <div id="resumeTextWrapper" class="pl-2">
          <h4>
            Find notices, articles, graphics, quickly, with a plain language.
            The best way to learn, and gain money.
          </h4>
        </div>
      </v-col>

      <v-col col="12" md="1"></v-col>
    </v-row>

    <!-- Caroulsel  -->

    <v-row class="noticeWrapper">
      <v-col col="12" md="12">
        <div class="titleSection mt-16">
          <img :src="btcGirando" alt="" width="90rem" />
          <h1 class="ml-7 mr-1 mt-4">Notices</h1>
          <img :src="btcGirando" alt="" width="90rem" />
        </div>

      
        <v-carousel
          class="mt-16"
          cycle
          height="40rem"
          hide-delimiter-background
          show-arrows-on-hover
        >
          <v-carousel-item v-for="(slide, i) in slides" :key="i">
            <v-row class="fill-height" align="end" justify="center">
              <img :src="colors[i]" width="100%"/>

              <div class="text-h2 mb-10 ml-4">
                <a href="#" target="_blank" rel="noopener noreferrer">{{
                  slide
                }}</a>
              </div>
            </v-row>
          </v-carousel-item>
        </v-carousel>


      </v-col>
    </v-row>

    
  </v-row>
</template>

<style>
/*Start title with typewritter*/

.initTextWrapper .mainTitle {
  font-size: 32pt;
  font-family: 'Roboto', sans-serif !important;
  font-style: italic;
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
  padding: 0.3rem;
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
  font-size: 10pt !important;
  background: rgba(255, 255, 255, 0) !important;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1) !important;
  backdrop-filter: blur(3.4px) !important;
  border: none !important;
}

.text-h2 a {
  color: rgba(255, 255, 255, 0.76);
  text-decoration: none;
}

.text-h2 a:hover {
  color: #fff;
}



.noticeWrapper .titleSection {
  display: flex;
  justify-content: center;
  align-items: center;
}

.noticeWrapper .titleSection h1 {
  font-size: 40pt;
  font-family: 'Roboto', sans-serif !important;
  font-style: italic;
}


</style>


<script>
import NavBar from '~/components/navBar.vue'
import RodaJequiti from '../components/rodaJequiti.vue'

export default {
  name: 'IndexPage',
  data() {
    return {
      btcGirando: 'img/btcGirando.gif',
      colors: [
        'img/imgTest3.jpg',
        'img/imgTest2.jpg',
        'img/imgTest5.jpg',
        'img/imgTest4.jpg',
        'img/imgTest6.jpg',
        'deep-purple accent-4',
      ],
      slides: [
        'Os touros Cardano perdem o fôlego após o hard fork Vasil: Queda de preço de 40% ADA.',
        'Binance vai queimar todas as taxas de negociação do LUNC após feedback da comunidade.',
        '4 sinais que indicam alta para o bitcoin na reta final de 2022 ',
        'Dogecoin sobe 18% após Musk dizer que Tesla vai aceitar moeda como pagamento',
        'USDT chegará a milhares de caixas eletrônicos no Brasil em novembro',
      ],
    }
  },
  components: { NavBar, RodaJequiti },

  methods: {
    /*
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
  }
*/
  },
}
</script>
