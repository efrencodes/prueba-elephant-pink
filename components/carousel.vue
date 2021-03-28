<template>
  <div class="carousel">
    <transition-group tag="div" :name="transitionName" class="slides-group">
      <div
        v-if="show"
        :key="current"
        class="slide image"
        :class="slides[current].className"
      >
        <div class="gradient"></div>
        <h2>DIAMONDS</h2>
        <hr />
        <p>Diamonds are the brightest starts and only</p>
        <p>the sky is the limit when it comes to</p>
        <p>achieving our jewels.</p>
      </div>
    </transition-group>
    <div class="btn btn-prev" aria-label="Previous slide" @click="slide(-1)">
      <i class="arrow"></i>
    </div>
    <div class="btn btn-next" aria-label="Next slide" @click="slide(1)">
      <i class="arrow"></i>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Carousel',
  data() {
    return {
      current: 0,
      direction: 1,
      transitionName: 'fade',
      show: false,
      slides: [
        { className: 'image' },
        { className: 'image' },
        { className: 'image' },
      ],
    }
  },
  mounted() {
    this.show = true
  },
  methods: {
    slide(dir) {
      this.direction = dir
      dir === 1
        ? (this.transitionName = 'slide-next')
        : (this.transitionName = 'slide-prev')
      const len = this.slides.length
      this.current = (this.current + (dir % len) + len) % len
    },
  },
}
</script>

<style lang="scss" scoped>
/* FADE IN */
.fade-enter-active {
  transition: opacity 1s;
}
.fade-enter {
  opacity: 0;
}
/* GO TO NEXT SLIDE */
.slide-next-enter-active,
.slide-next-leave-active {
  transition: transform 0.5s ease-in-out;
}
.slide-next-enter {
  transform: translate(100%);
}
.slide-next-leave-to {
  transform: translate(-100%);
}
/* GO TO PREVIOUS SLIDE */
.slide-prev-enter-active,
.slide-prev-leave-active {
  transition: transform 0.5s ease-in-out;
}
.slide-prev-enter {
  transform: translate(-100%);
}
.slide-prev-leave-to {
  transform: translate(100%);
}
.image {
  background-image: url('https://res.cloudinary.com/efrenmartinez/image/upload/v1616908825/prueba-elephant-pink/images/jewelry-carousel_zlfidk.jpg');
  background-size: cover;
}
.btn {
  z-index: 10;
  cursor: pointer;
  border: none;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 105px;
  height: 20px;
  position: absolute;
  top: calc(50% - 35px);
  left: 1%;
  transition: transform 0.3s ease-in-out;
  user-select: none;
  background-color: transparent;
  &-next {
    left: auto;
    right: 1%;
  }
  &-prev {
    i {
      transform: rotate(180deg);
    }
  }
}
.btn:hover {
  transform: scale(1.1);
}

h2 {
  color: var(--color-white);
  font-size: 30px;
  font-family: Didot;
  line-height: 25px;
  text-transform: uppercase;
  z-index: 10;
}
hr {
  width: 12%;
  z-index: 10;
  background: var(--color-white);
  height: 1px;
  margin-top: 20px;
  margin-bottom: 20px;
}
p {
  z-index: 10;
  color: var(--color-white);
  line-height: 15px;
}
</style>
