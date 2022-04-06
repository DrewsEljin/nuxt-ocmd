<template>
  <div class="wrapper">
    <div class="carousel" :style="{'margin-left': '-' + 100*index +'%'}">
      <div v-for="item in slides" :key="item.id" class="item">
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
          src: 'https://cdn.pixabay.com/photo/2015/12/12/15/24/amsterdam-1089646_1280.jpg'
        },
        {
          id: 2,
          src: 'https://cdn.pixabay.com/photo/2016/02/17/23/03/usa-1206240_1280.jpg'
        },
        {
          id: 3,
          src: 'https://cdn.pixabay.com/photo/2016/12/04/19/30/berlin-cathedral-1882397_1280.jpg'
        }
      ],
      index: 0
    }
  },
  methods: {
    prev () {
      if (this.index !== 0) {
        this.index -= 1
      }
    },
    next () {
      if (this.index < this.slides.length - 1) {
        this.index += 1
      } else {
        this.index = 0
      }
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
}
</style>
