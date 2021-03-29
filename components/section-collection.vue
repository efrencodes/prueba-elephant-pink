<template>
  <section class="section-collection container text-center">
    <h1>
      <hr />
      OUR COLLECTION
      <hr />
    </h1>
    <p>
      Specially crafted with utmost of precision and care, our dreamy jewels are
      meant to make your wishes come true.
    </p>
    <div class="section-collection-card" style="margin-top: 60px">
      <template v-for="i in 3">
        <Card :key="i" :index="i" />
      </template>
    </div>
    <div
      v-if="isVisible"
      class="section-collection-card"
      style="margin-top: 30px"
    >
      <template v-for="i in 3">
        <Card :key="i" :index="i + 3" />
      </template>
    </div>
    <button class="btn" @click="isVisible = !isVisible">VIEW ALL</button>
    <Contact @open="$emit('open')" />
  </section>
</template>

<script>
export default {
  name: 'SectionCollection',
  data() {
    return {
      isVisible: false,
    }
  },
}
</script>

<style lang="scss" scoped>
.section-collection {
  padding: 85px 100px 20px 100px;
  h1 {
    font-family: Didot;
    color: var(--color-black);
    letter-spacing: 4px;
    font-size: 1.8em;
    font-weight: normal;
    hr {
      display: inline-block;
      width: 36%;
      margin: 5px 10px;
      border-top: 1px solid #e5e5e5;
    }
  }
  hr.title::after {
    content: 'OUR COLLECTION';
    display: inline-block;
    position: relative;
    top: -0.7em;
    font-size: 1.8em;
    padding: 0 10px;
    font-family: Didot;
    background: var(--color-white);
    color: var(--color-black);
    letter-spacing: 4px;
  }
  p {
    margin-top: 30px;
    color: var(--color-gray);
    font-size: 12px;
    width: 500px;
    margin: 30px auto;
  }
  &-card {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    column-gap: 15px;
  }
  button {
    margin-top: 80px;
  }
}
</style>
