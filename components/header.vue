<template>
  <header class="">
    <div
      class="container flex align-center justify-evenly"
      style="height: 100%"
    >
      <button
        class="btn-icon flex justify-center align-center"
        style="margin-top: -6px"
      >
        <i class="lock"></i>Login
      </button>
      <div class="header-btn flex">
        <button
          class="btn-menu flex column align-center active"
          style="margin-top: 6px"
        >
          home<i class="diamond-active"></i>
        </button>
        <button class="btn-menu flex column align-center">about</button>
        <img
          src="https://res.cloudinary.com/efrenmartinez/image/upload/v1615793192/prueba-elephant-pink/images/logotipo-black_iwrwae.svg"
          alt="Logotipo"
        />
        <button class="btn-menu flex column align-center">jewels</button>
        <button class="btn-menu flex column align-center">contact</button>
      </div>
      <div class="header-right flex justify-start">
        <select>
          <option value="0">EN</option>
          <option value="1">ES</option>
        </select>
        <button class="btn-search" style="margin-left: 5px">
          <i class="search"></i>
        </button>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
}
</script>
