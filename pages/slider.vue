<template>
  <div class="wrapper">
    <div class="carousel" :style="index">
      <div
        v-for="item in slides"
        :key="item.id"
        class="item"
        :class="item.class"
      >
        <img :src="item.src" alt="">
      </div>
    </div>
    <nav>
      <button @click="prev">
        prev
      </button>
      <button @click="next">
        next
      </button>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'SliderPage',
  layout: 'storeLayout',
  data () {
    return {
      slides: [
        {
          id: 1,
          src: 'https://cdn.pixabay.com/photo/2015/12/12/15/24/amsterdam-1089646_1280.jpg',
          class: 'slide-active'
        },
        {
          id: 2,
          src: 'https://cdn.pixabay.com/photo/2016/02/17/23/03/usa-1206240_1280.jpg',
          class: 'slide-next'
        },
        {
          id: 3,
          src: 'https://cdn.pixabay.com/photo/2016/12/04/19/30/berlin-cathedral-1882397_1280.jpg'
        },
        {
          id: 4,
          src: 'https://cdn.pixabay.com/photo/2015/12/12/15/24/amsterdam-1089646_1280.jpg'
        },
        {
          id: 5,
          src: 'https://cdn.pixabay.com/photo/2016/02/17/23/03/usa-1206240_1280.jpg'
        },
        {
          id: 6,
          src: 'https://cdn.pixabay.com/photo/2016/12/04/19/30/berlin-cathedral-1882397_1280.jpg',
          class: 'slide-prev'
        }
      ],
      index: 0
    }
  },
  methods: {
    prev () {
      if (this.index > 0) {
        this.clear()
        this.slides[this.index - 1].class = 'slide-active'
        this.slides[this.index].class = 'slide-next'
        this.index -= 1
        if (this.slides[this.index - 1]) {
          this.slides[this.index - 1].class = 'slide-prev'
        } else {
          this.slides[this.slides.length - 1].class = 'slide-prev'
        }
      } else {
        this.clear()
        this.slides[this.slides.length - 1].class = 'slide-active'
        this.slides[0].class = 'slide-next'
        this.index = this.slides.length - 1
        this.slides[this.index - 1].class = 'slide-prev'
      }
    },
    next () {
      if (this.index < this.slides.length - 1) {
        this.clear()
        this.slides[this.index + 1].class = 'slide-active'
        if (this.slides[this.index + 2]) {
          this.slides[this.index + 2].class = 'slide-next'
        }
        this.index += 1
        this.slides[this.index - 1].class = 'slide-prev'
      } else {
        this.clear()
        this.index = 0
        this.slides[this.index].class = 'slide-active'
        this.slides[this.index + 1].class = 'slide-next'
        this.slides[this.slides.length - 1].class = 'slide-prev'
      }
      if (this.index === this.slides.length - 1) {
        this.slides[0].class = 'slide-next'
      }
    },
    clear () {
      this.slides.forEach(function (v) {
        delete v.class
      })
    }
  }
}
</script>

<style scoped>
img {
  width: 500px;
  height: 300px;
}
.carousel {
  margin-top: 100px;
  display: flex;
  transition: 0.3s;
  position: relative;
  height: 300px;
}
.wrapper {
  max-width: 500px;
  margin: 0 auto;
  overflow: hidden;
}
nav {
  text-align: center;
}

nav button {
  padding: 10px;
  cursor: pointer;
  background: #000;
  color: #fff;
  border-radius: 10px;
  margin-top: 30px;
}

.item {
  display: none;
  position: absolute;
  transition: 0.3s;
}

.slide-prev {
  left: -100%;
}
.slide-next {
  left: 100%;
}

.slide-active {
  left: 0;
}

.slide-prev , .slide-active , .slide-next {
  display: block;
}
</style>
