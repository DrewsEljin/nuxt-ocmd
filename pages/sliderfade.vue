<template>
  <div>
    <transition-group name="fade" tag="div">
      <div v-for="i in [index]" :key="i" class="item">
        <img :src="currentImg">
      </div>
    </transition-group>
    <button class="prev" @click="prev">
      prev
    </button>
    <button class="next" @click="next">
      next
    </button>
  </div>
</template>

<script>
export default {
  name: 'SliderFade',
  layout: 'storeLayout',
  data () {
    return {
      images: [
        'https://cdn.pixabay.com/photo/2015/12/12/15/24/amsterdam-1089646_1280.jpg',
        'https://cdn.pixabay.com/photo/2016/02/17/23/03/usa-1206240_1280.jpg',
        'https://cdn.pixabay.com/photo/2016/12/04/19/30/berlin-cathedral-1882397_1280.jpg'
      ],
      index: 0
    }
  },

  computed: {
    currentImg () {
      this.cycle()
      return this.images[this.index]
    }
  },

  methods: {
    cycle () {
      if (this.index === this.images.length) {
        this.index = 0
      }
    },
    next () {
      this.index += 1
    },
    prev () {
      this.index -= 1
    }
  }
}
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: all 0.9s ease;
  overflow: hidden;
  visibility: visible;
  position: absolute;
  width: 100%;
  opacity: 1;
}
.item {
  text-align: center;
}

.fade-enter,
.fade-leave-to {
  visibility: hidden;
  width: 100%;
  opacity: 0;
}

img {
  height: 600px;
  max-width: 100%;
}

 button {
  position: absolute;
  padding: 10px;
  cursor: pointer;
  background: #000;
  color: #fff;
  border-radius: 10px;
}

.prev , .next {
  top: 25%;
  cursor: pointer;

}
.prev {
  left: 15px;

}

.next {
  right: 15px;
}
</style>
