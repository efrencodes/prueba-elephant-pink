<template>
  <div>
    <Header />
    <Carousel />
    <SectionCollection />
    <Footer />
  </div>
</template>

<script>
export default {
  name: 'PageIndex',
  data() {
    return {
      active: true,
    }
  },
  mounted() {
    window.addEventListener('scroll', this.onScroll)
  },
  destroyed() {
    window.removeEventListener('scroll', this.onScroll)
  },
  methods: {
    onScroll() {
      // eslint-disable-next-line no-console
      console.log(window.scrollY > 100)
      // eslint-disable-next-line no-console
      console.log(window.scrollY > 0)
      this.active = window.scrollY < 100 || window.scrollY < 0
    },
  },
}
</script>
