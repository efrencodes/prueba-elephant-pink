<template>
  <div class="contact flex align-center">
    <div class="contact-left">
      <h3>CONTACT US <span>Diamonds</span></h3>
    </div>
    <div class="contact-middle text-left">
      <p>
        Sed ut perspiciatis unde omnis iste natus error sit voluptatem
        accosantium doloremque laudantium, totam rem aperiam eaque ipsa quae ab
        illo inventore.
      </p>
    </div>
    <div class="contact-right">
      <button class="btn" @click="$emit('open')">Contact</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Contact',
}
</script>

<style lang="scss" scoped>
.contact {
  box-shadow: rgba(0, 0, 0, 0.04) 0px 3px 5px;
  margin-bottom: 40px;
  margin-top: 40px;
  padding: 20px 40px;

  &-left {
    width: 500px;
    text-align: initial;
    h3 {
      font-size: 20px;
      font-weight: 600;
      color: var(--color-golden);
      span {
        font-family: 'Blesing';
        font-size: 26px;
        font-weight: 400;
        color: var(--color-black);
      }
    }
  }
}
</style>
