<template>
  <div>
    <Header :class="{ fixed: !active }" />
    <Carousel />
    <SectionCollection @open="showModal = true" />
    <Footer />
    <Modal v-if="showModal" @close="showModal = false">
      <h3 slot="header" class="h3-modal">CLOSE</h3>
      <template slot="body">
        <h4 class="h4-modal">Contact</h4>
        <p class="p-modal">
          The sparkles of the diamonds on this powerful ring symbolize the
          strength of beaty
        </p>
        <form action="#">
          <input
            v-model="form.name"
            type="text"
            class="input-primary"
            placeholder="Name"
            required
          />
          <input
            v-model="form.email"
            type="email"
            class="input-primary"
            placeholder="Email"
            required
          />
          <textarea
            v-model="form.message"
            cols="30"
            rows="6"
            placeholder="Your message here."
            class="textarea-primary"
            resize
          ></textarea>
        </form>
        <p v-if="showMesage" class="p-error">Unexpected server error_</p>
      </template>
      <template slot="footer">
        <button class="btn-send" @click="onSubmit">SEND</button>
      </template>
    </Modal>
  </div>
</template>

<script>
export default {
  name: 'PageIndex',
  data() {
    return {
      active: true,
      showModal: false,
      form: {
        name: null,
        email: null,
        message: null,
      },
      showMesage: false,
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
      this.active = window.scrollY < 200 || window.scrollY < 0
    },
    onSubmit() {
      if (
        this.form.name !== null &&
        this.form.email !== null &&
        this.form.massage !== null
      ) {
        this.showModal = false
      } else {
        this.showMesage = true
      }
    },
  },
}
</script>

<style lang="scss" scoped>
.fixed {
  transition: background-color 250ms ease-in-out;
  position: fixed;
  z-index: 2000;
  width: 100%;
  background-color: white;
}
.h4-modal {
  font-family: Didot;
  font-size: 25px;
  text-transform: uppercase;
  letter-spacing: 5px;
  font-weight: lighter;
}
.p-modal {
  margin-top: 20px;
  font-size: 12px;
  line-height: 20px;
}
.p-error {
  color: red;
}
</style>
