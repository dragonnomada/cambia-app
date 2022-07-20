<template>
  <div class="inicio">
    <img
      alt=""
      class="inicio-fondo"
      src="https://static.overlay-tech.com/assets/0affa40c-205a-405d-aeb2-4b67857acf80.svg"
    />
    <div class="logo-inicio">
      <div class="logo-inicio-circulo-menor"></div>
      <img
        alt=""
        class="logo-cambia"
        src="https://static.overlay-tech.com/assets/4301fc5f-1ebe-4d6f-a6e6-e5378683de62.svg"
      />
    </div>
    <img
      alt=""
      class="logo-citibanamex"
      src="https://static.overlay-tech.com/assets/4208fe9e-0b1b-4dd3-badd-22c1f5e1d3b5.svg"
    />
  </div>
</template>

<script>
export default {
  name: "Inicio"
};
</script>

<style lang="scss" scoped>
.inicio {
  background-color: rgba(255, 255, 255, 1);
  position: relative;
  width: 100%;
  height: 100vh;
}
.inicio-fondo {
  width: 100%;
  height: 100%;
  position: relative;
  object-fit: cover;
}
.logo-inicio {
  background-color: rgba(255, 255, 255, 0.15);
  border-radius: 50%;
  padding: 29.5px 30px 33.5px 33px;
  display: flex;
  align-items: flex-start;
  position: absolute;
  left: calc(50% - 144px);
  top: 210.5px;
}
.logo-inicio-circulo-menor {
  width: 225px;
  height: 225px;
  background-color: rgba(255, 255, 255, 0.35);
  border-radius: 50%;
  position: relative;
}
.logo-cambia {
  width: 210px;
  height: 58.98px;
  position: absolute;
  left: 40px;
  top: 113.5px;
}
.logo-citibanamex {
  width: 142px;
  height: 22px;
  position: absolute;
  left: calc(50% - 71px);
  bottom: 46px;
}
</style>