<template>
  <article class="card flex column justify-center text-center align-center">
    <img
      src="https://res.cloudinary.com/efrenmartinez/image/upload/v1616974459/prueba-elephant-pink/images/shutterstock_sfa9yt.jpg"
      alt="Anillo de plata"
    />
    <h1>diamond {{ index }}</h1>
    <hr />
    <p>
      The sparkles of the diamonds on this powerful ring symbolize the strength
      of beaty
    </p>
    <i class="diamond-active"></i>
  </article>
</template>

<script>
export default {
  name: 'Card',
  props: {
    index: {
      type: Number,
      required: true,
    },
  },
}
</script>

<style lang="scss" scoped>
.card {
  padding: 20px;
  img {
    text-align: center;
    max-width: 180px;
    width: 100%;
  }
  h1 {
    font-size: 20px;
    font-family: Didot;
    font-weight: lighter;
    margin-top: 30px;
    text-transform: uppercase;
    margin-bottom: 20px;
  }
  p {
    margin-top: 20px;
    color: var(--color-gray);
  }
  hr {
    width: 50%;
    background: hsla(0, 0%, 76.9%, 0.36);
  }
  i {
    margin-top: 25px;
  }
}
</style>
