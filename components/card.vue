<template>
  <article class="card flex column justify-center text-center align-center">
    <img
      src="https://res.cloudinary.com/efrenmartinez/image/upload/v1615792654/prueba-elephant-pink/images/shutterstock_bizeto.jpg"
      alt="Anillo de plata"
    />
    <h4>diamond 3</h4>
    <hr />
    <p>
      The sparkles of the diamonds on this powerful ring symbolize the strength
      of beaty
    </p>
  </article>
</template>

<script>
export default {
  name: 'Card',
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
  h4 {
    font-size: 20px;
    font-family: Didot;
    line-height: 25px;
    text-transform: uppercase;
    font-weight: lighter;
    margin-top: 30px;
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
}
</style>
