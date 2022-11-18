<template>
  <v-row class="d-flex flex-column">
    <RodaJequiti />
    <NavBar />

    <!-- Start title with typewritter  -->
    <v-row class="mt-16 initTextWrapper">
      <h1 id="greenWord" class="mainTitle">EXPLORE</h1>
      <h1 class="typeWriter mainTitle">
        THE BEST INFO PLACE FOR BEGGINERS AND CRIPTOLOVERS!
      </h1>
    </v-row>

    <!-- First icons  -->

    <v-row>
      <v-col col="12" md="1"></v-col>

      <v-col
        class="iconsWrapper mt-10 mb-6"
        col="12"
        md="10"
        sm="6"
        justify-content="center"
      >
        <div class="iconContentWrapper">
          <v-icon size="50" color="teal" class="iconSelf mr-2"
            >mdi-book-edit</v-icon
          >
          <div class="textIconWrapper">
            <h2>100+</h2>
            <h4>Articles</h4>
          </div>
        </div>

        <div class="iconContentWrapper">
          <v-icon size="50" color="teal" class="iconSelf mr-2"
            >mdi-newspaper</v-icon
          >
          <div class="textIconWrapper">
            <h2>10+</h2>
            <h4>Notices/day</h4>
          </div>
        </div>

        <div class="iconContentWrapper">
          <v-icon size="50" color="teal" class="iconSelf mr-2"
            >mdi-earth</v-icon
          >
          <div class="textIconWrapper">
            <h2>1000+</h2>
            <h4>Views</h4>
          </div>
        </div>

        <div id="resumeTextWrapper" class="pl-2">
          <h3>
            Find notices, articles, graphics, quickly, with a plain language.
            The best way to learn, and gain money.
          </h3>
        </div>
      </v-col>

      <v-col col="12" md="1"></v-col>
    </v-row>

    <!-- Caroulsel  -->

    <v-row class="mt-16 mb-16" align="center" justify="center">
      <img :src="btcGirando" alt="" width="90rem" />
      <h1 class="ml-7 mr-1 mt-4 titleSection">Notices</h1>
      <img :src="btcGirando" alt="" width="90rem" />
    </v-row>

    <v-carousel
      class="caro mb-10"
      cycle
      height="35rem"
      hide-delimiter-background
      show-arrows-on-hover
    >
      <v-carousel-item v-for="(slide, i) in slides" :key="i">
        <v-row class="fill-height" align="end" justify="center">
          <img :src="colors[i]" width="100%" />

          <div class="text-h2 mb-10 ml-4">
            <a href="#" target="_blank" rel="noopener noreferrer">{{
              slide
            }}</a>
          </div>
        </v-row>
      </v-carousel-item>
    </v-carousel>

    <!-- Articles -->

    <v-row class="mt-16 mb-10">
      <v-col col="12" md="12" sm="6">
        <v-row class="mt-16 mb-16" align="center" justify="center">
          <img :src="btcGirando" alt="" width="90rem" />
          <h1 class="ml-7 mr-1 mt-4 titleSection">Articles</h1>
          <img :src="btcGirando" alt="" width="90rem" />
        </v-row>

        <v-row>
          <v-card class="mx-auto" max-width="400">
            <v-img :src="colors[2]" height="200px"></v-img>

            <v-card-title> Bitcoin </v-card-title>

            <v-card-subtitle> The main Cripto </v-card-subtitle>

            <v-card-actions>
              <v-btn color="teal" text> Explore </v-btn>

              <v-spacer></v-spacer>

              <v-btn icon @click="show = !show">
                <v-icon>{{
                  show ? 'mdi-chevron-up' : 'mdi-chevron-down'
                }}</v-icon>
              </v-btn>
            </v-card-actions>

            <v-expand-transition>
              <div v-show="show">
                <v-divider></v-divider>

                <v-card-text>
                  It is a free and decentralized cryptocurrency, an electronic
                  money for peer-to-peer financial transactions (without
                  intermediaries), Bitcoin is considered the world's first
                  digital currency decentralized, constituting an alternative
                  economic system, and responsible for the resurgence of the
                  free banking.
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>

          <v-card class="mx-auto" max-width="400">
            <v-img :src="colors[6]" height="200px"></v-img>

            <v-card-title> Ethereum </v-card-title>

            <v-card-subtitle> The main Blockchain </v-card-subtitle>

            <v-card-actions>
              <v-btn color="teal" text> Explore </v-btn>

              <v-spacer></v-spacer>

              <v-btn icon @click="show = !show">
                <v-icon>{{
                  show ? 'mdi-chevron-up' : 'mdi-chevron-down'
                }}</v-icon>
              </v-btn>
            </v-card-actions>

            <v-expand-transition>
              <div v-show="show">
                <v-divider></v-divider>

                <v-card-text>
                  Ethereum is a technology that encompasses digital money,
                  global payments and investments. The community has created a
                  booming digital economy, new ways to make money online, and
                  more. It's open to anyone, anywhere in the world – all you
                  need is the Internet.
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>

          <v-card class="mx-auto" max-width="400">
            <v-img :src="colors[5]" height="200px"></v-img>

            <v-card-title> Terra Luna </v-card-title>

            <v-card-subtitle> The Do Kwon Platform </v-card-subtitle>

            <v-card-actions>
              <v-btn color="teal" text> Explore </v-btn>

              <v-spacer></v-spacer>

              <v-btn icon @click="show = !show">
                <v-icon>{{
                  show ? 'mdi-chevron-up' : 'mdi-chevron-down'
                }}</v-icon>
              </v-btn>
            </v-card-actions>

            <v-expand-transition>
              <div v-show="show">
                <v-divider></v-divider>

                <v-card-text>
                  LUNA (Terra) is Earth's native governance token, stablecoin
                  creation platform. The main feature of this protocol is the
                  possibility for the user to associate cryptocurrencies with
                  other assets, helping to solve problems such as fluctuation in
                  values. Through the financial user of other stable assets
                  (DemonFi), the project allows, among others, that the user in
                  other stable assets and performs fee submissions.
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-row>
      </v-col>
    </v-row>

    <!-- Graphics -->

    <v-row>
      <v-col class="mt-16" col="12" md="12" sm="6">
        <v-row class="mt-16 mb-16" align="center" justify="center">
          <img :src="btcGirando" alt="" width="90rem" />
          <h1 class="ml-7 mr-1 mt-4 titleSection">Main Info</h1>
          <img :src="btcGirando" alt="" width="90rem" />
        </v-row>
        <Graphic />
      </v-col>
    </v-row>

    <!-- New (testing) -->

    <v-row>
      <v-col class="mt-16" col="12" md="12" sm="6">
        <v-row class="mt-16 mb-16" align="center" justify="center">
          <img :src="btcGirando" alt="" width="90rem" />
          <h1 class="ml-7 mr-1 mt-4 titleSection">New</h1>
          <!--Colocar emoji-->
          <img :src="btcGirando" alt="" width="90rem" />
        </v-row>

        <v-row class="twitterWrapper">
          <v-card class="mx-auto" color="black" dark max-width="400">
            <v-card-title>
              <v-icon large left color="#26c6da"> mdi-twitter </v-icon>
              <span class="text-h6 font-weight-light">Twitter</span>
            </v-card-title>

            <v-card-text class="text-h5 font-weight-bold">
              "Tesla will make some merch buyable with Doge & see how it goes."
            </v-card-text>

            <v-card-actions>
              <v-list-item class="grow">
                <v-list-item-avatar color="grey darken-3">
                  <v-img class="elevation-6" alt="" :src="imgTwitter"></v-img>
                </v-list-item-avatar>

                <v-list-item-content>
                  <v-list-item-title>Elon Musk</v-list-item-title>
                </v-list-item-content>

                <v-row align="center" justify="end">
                  <v-icon class="mr-1"> mdi-heart </v-icon>
                  <span class="subheading mr-2">217.5k</span>
                  <span class="mr-1">·</span>
                  <v-icon class="mr-1"> mdi-share-variant </v-icon>
                  <span class="subheading">36.7k</span>
                </v-row>
              </v-list-item>
            </v-card-actions>
          </v-card>

          <v-card class="mx-auto" color="black" dark max-width="400">
            <v-card-title>
              <v-icon large left color="#26c6da"> mdi-twitter </v-icon>
              <span class="text-h6 font-weight-light">Twitter</span>
            </v-card-title>

            <v-card-text class="text-h5 font-weight-bold">
              "Tesla will make some merch buyable with Doge & see how it goes."
            </v-card-text>

            <v-card-actions>
              <v-list-item class="grow">
                <v-list-item-avatar color="grey darken-3">
                  <v-img class="elevation-6" alt="" :src="imgTwitter"></v-img>
                </v-list-item-avatar>

                <v-list-item-content>
                  <v-list-item-title>Elon Musk</v-list-item-title>
                </v-list-item-content>

                <v-row align="center" justify="end">
                  <v-icon class="mr-1"> mdi-heart </v-icon>
                  <span class="subheading mr-2">217.5k</span>
                  <span class="mr-1">·</span>
                  <v-icon class="mr-1"> mdi-share-variant </v-icon>
                  <span class="subheading">36.7k</span>
                </v-row>
              </v-list-item>
            </v-card-actions>
          </v-card>

          <v-card class="mx-auto" color="black" dark max-width="400">
            <v-card-title>
              <v-icon large left color="#26c6da"> mdi-twitter </v-icon>
              <span class="text-h6 font-weight-light">Twitter</span>
            </v-card-title>

            <v-card-text class="text-h5 font-weight-bold">
              "Tesla will make some merch buyable with Doge & see how it goes."
            </v-card-text>

            <v-card-actions>
              <v-list-item class="grow">
                <v-list-item-avatar color="grey darken-3">
                  <v-img class="elevation-6" alt="" :src="imgTwitter"></v-img>
                </v-list-item-avatar>

                <v-list-item-content>
                  <v-list-item-title>Elon Musk</v-list-item-title>
                </v-list-item-content>

                <v-row align="center" justify="end">
                  <v-icon class="mr-1"> mdi-heart </v-icon>
                  <span class="subheading mr-2">217.5k</span>
                  <span class="mr-1">·</span>
                  <v-icon class="mr-1"> mdi-share-variant </v-icon>
                  <span class="subheading">36.7k</span>
                </v-row>
              </v-list-item>
            </v-card-actions>
          </v-card>
        </v-row>
      </v-col>
    </v-row>

    <!-- Stories -->

    <v-row>
      <v-col class="mt-16" col="12" md="12" sm="6">
        <v-row class="mt-16 mb-16" align="center" justify="center">
          <img :src="btcGirando" alt="" width="90rem" />
          <h1 class="ml-7 mr-1 mt-4 titleSection">TokenPedia</h1>
          <img :src="btcGirando" alt="" width="90rem" />
        </v-row>

        <v-row>
          <v-dialog v-model="dialog" width="500">
            <template v-slot:activator="{ on, attrs }">
              <v-card class="mx-auto" max-width="350" v-bind="attrs" v-on="on">
                <v-img
                  class="white--text align-end"
                  height="450px"
                  :src="stories[0]"
                >
                  <v-card-title>O que é Blockchain </v-card-title>
                </v-img>
              </v-card>
            </template>

            <v-card>
              <!-- 
              <v-card-title class="text-h5 grey lighten-2">
                Privacy Policy
              </v-card-title>

              <v-card-text>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
                eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
                enim ad minim veniam, quis nostrud exercitation ullamco laboris
                nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor
                in reprehenderit in voluptate velit esse cillum dolore eu fugiat
                nulla pariatur. Excepteur sint occaecat cupidatat non proident,
                sunt in culpa qui officia deserunt mollit anim id est laborum.
              </v-card-text>

              <v-divider></v-divider>

              <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn color="primary" text @click="dialog = false">
                  I accept
                </v-btn>
              </v-card-actions>
-->

            </v-card>
          </v-dialog>

          <v-card class="mx-auto" max-width="350">
            <v-img
              class="white--text align-end"
              height="450px"
              :src="stories[1]"
            >
              <v-card-title>O que é NFT</v-card-title>
            </v-img>
          </v-card>

          <v-card class="mx-auto" max-width="350">
            <v-img
              class="white--text align-end"
              height="450px"
              :src="stories[2]"
            >
              <v-card-title>O que é Smart Contract</v-card-title>
            </v-img>
          </v-card>
        </v-row>
      </v-col>
    </v-row>

    <v-row>
      <Storie/>
    </v-row>

  </v-row>
</template>

<style>
/*Start title with typewritter*/

.initTextWrapper h1 {
  width: 100%;
  text-align: center;
  font-size: 42pt !important;
  opacity: 0;
}
.initTextWrapper .mainTitle {
  font-size: 32pt;
  font-family: 'Roboto', sans-serif !important;
  font-style: italic;
}

.initTextWrapper .mainTitle::after {
  content: '|';
  opacity: 1;
  animation: pisc 0.7s infinite;
}

#greenWord {
  color: teal;
}

#greenWord::after {
  content: '|';
  margin-left: 0.4rem;
  opacity: 1;
  animation: pisc 0.7s infinite;
}

@keyframes pisc {
  0%,
  100% {
    opacity: 1;
  }
  50% {
    opacity: 0;
  }
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

.caro {
  border-radius: 10px;
}

.text-h2 {
  position: absolute;
  font-size: 10pt !important;
  background: rgba(255, 255, 255, 0) !important;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1) !important;
  backdrop-filter: blur(3.4px) !important;
  border: none !important;
  width: 90%;
}

.text-h2 a {
  color: rgba(255, 255, 255, 0.76);
  text-decoration: none;
}

.text-h2 a:hover {
  color: #fff;
}

.titleSection {
  font-size: 40pt;
  font-family: 'Roboto', sans-serif !important;
  font-style: italic;
}

/* Articles */

.articleWrapper {
  display: flex;
}
</style>


<script>
import NavBar from '~/components/navBar.vue'
import RodaJequiti from '~/components/rodaJequiti.vue'
import Graphic from '~/components/mainGraphs.vue'
import Storie from '~/components/storie.vue'

export default {
  name: 'IndexPage',
  data() {
    return {
      btcGirando: 'img/btcGirando.gif',
      imgTwitter: 'img/imgTwitter.jpg',
      colors: [
        'img/imgTest3.jpg',
        'img/imgTest2.jpg',
        'img/imgTest5.jpg',
        'img/imgTest4.jpg',
        'img/imgTest6.jpg',
        'img/imgTest7.jpg',
        'img/imgtest8.jpg',
      ],
      slides: [
        'Os touros Cardano perdem o fôlego após o hard fork Vasil: Queda de preço de 40% ADA.',
        'Binance vai queimar todas as taxas de negociação do LUNC após feedback da comunidade.',
        '4 sinais que indicam alta para o bitcoin na reta final de 2022 ',
        'Dogecoin sobe 18% após Musk dizer que Tesla vai aceitar moeda como pagamento',
        'USDT chegará a milhares de caixas eletrônicos no Brasil em novembro',
      ],
      stories: [
        'img/imgTestStorie1.jpg',
        'img/imgTestStorie2.jfif',
        'img/imgTestStorie3.jpg',
      ],
      show: false,
      dialog: false,
    }
  },

  mounted() {
    this.typeWriter()
  },
  components: { NavBar, RodaJequiti, Graphic },

  methods: {
    typeWriter() {
      const elementTitle1 = document.querySelector('#greenWord')
      const elementTitle2 = document.querySelector('.typeWriter')

      const arrGreenWord = elementTitle1.innerHTML.split('')
      const arrPhrase = elementTitle2.innerHTML.split('')
      elementTitle1.innerHTML = ''
      elementTitle2.innerHTML = ''
      elementTitle1.style.opacity = '1'
      elementTitle2.style.opacity = '1'

      arrGreenWord.forEach((element, ind) => {
        setTimeout(() => {
          setTimeout(() => (elementTitle1.innerHTML += element), 75 * ind)
        })
      }, 2000)

      setTimeout(() => {
        arrPhrase.forEach((element, ind) => {
          setTimeout(() => (elementTitle2.innerHTML += element), 75 * ind)
        })
      }, 1100)
    },
  },
}
</script>
