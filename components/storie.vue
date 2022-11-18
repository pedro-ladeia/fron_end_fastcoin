<template>
  <v-row>
    <div data-slide="slide" class="slide">
      <div class="slide-items">
        <v-img :src="imgStories[0]"></v-img>
        <v-img :src="imgStories[1]"></v-img>
        <v-img :src="imgStories[2]"></v-img>
        <v-img :src="imgStories[3]"></v-img>
      </div>
      <nav class="slide-nav">
        <div class="slide-thumb"></div>
        <button class="slide-prev">Anterior</button>
        <button class="slide-next">Próximo</button>
      </nav>
    </div>
  </v-row>
</template>



<style>
img {
  max-width: 100%;
  display: block;
}

.slide {
  max-width: 100%;
  max-height: 100%;
  margin: 20px auto;
  display: grid;
  box-shadow: 0 4px 20px 2px rgba(0, 0, 0, 0.4);
}

.slide-items {
  position: relative;
  grid-area: 1/1;
  border-radius: 5px;
  overflow: hidden;
}

.slide-nav {
  grid-area: 1/1;
  z-index: 1;
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: auto 1fr;
}

.slide-nav button {
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
  opacity: 0;
}

.slide-items > * {
  position: absolute;
  top: 0px;
  opacity: 0;
  pointer-events: none;
}

.slide-items > .active {
  position: relative;
  opacity: 1;
  pointer-events: initial;
}

.slide-thumb {
  display: flex;
  grid-column: 1 / 3;
}

.slide-thumb > span {
  flex: 1;
  display: block;
  height: 3px;
  background: rgba(0, 0, 0, 0.4);
  margin: 5px;
  border-radius: 3px;
  overflow: hidden;
}

.slide-thumb > span.active::after {
  content: '';
  display: block;
  height: inherit;
  background: rgba(255, 255, 255, 0.9);
  border-radius: 3px;
  transform: translateX(-100%);
  animation: thumb 5s forwards linear;
}

@keyframes thumb {
  to {
    transform: initial;
  }
}
</style>

<script>
import storieJs from '~/plugins/storie'

export default {
  data() {
    return {
      imgStories: [
        'img/img-stories/1.png',
        'img/img-stories/2.png',
        'img/img-stories/3.png',
        'img/img-stories/4.png',
      ],
    }
  },
  components: { storieJs },
  methods: {
    
  }
}

class SlideStories {
  constructor(id) {
    this.slide = document.querySelector(`[data-slide="${id}"]`)
    this.active = 0
    this.init()
  }
  activeSlide(index) {
    this.active = index
    this.items.forEach((item) => item.classList.remove('active'))
    this.items[index].classList.add('active')
    this.thumbItems.forEach((item) => item.classList.remove('active'))
    this.thumbItems[index].classList.add('active')
    this.autoSlide()
  }

  prev() {
    if (this.active > 0) {
      this.activeSlide(this.active - 1)
    } else {
      this.activeSlide(this.items.length - 1)
    }
  }

  next() {
    if (this.active < this.items.length - 1) {
      this.activeSlide(this.active + 1)
    } else {
      this.activeSlide(0)
    }
  }

  addNavigation() {
    const nextBtn = this.slide.querySelector('.slide-next')
    const prevBtn = this.slide.querySelector('.slide-prev')
    nextBtn.addEventListener('click', this.next)
    prevBtn.addEventListener('click', this.prev)
  }

  addThumbItems() {
    this.items.forEach(() => (this.thumb.innerHTML += `<span></span>`))
    this.thumbItems = Array.from(this.thumb.children)
  }

  autoSlide() {
    clearTimeout(this.timeout)
    this.timeout = setTimeout(this.next, 5000)
  }

  init() {
    this.next = this.next.bind(this)
    this.prev = this.prev.bind(this)
    this.items = this.slide.querySelectorAll('.slide-items > *')
    this.thumb = this.slide.querySelector('.slide-thumb')
    this.addThumbItems()
    this.activeSlide(0)
    this.addNavigation()
  }

}
new SlideStories('slide')
</script>