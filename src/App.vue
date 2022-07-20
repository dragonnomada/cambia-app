<script setup>
// import Inicio from './components/Inicio.vue'
import Login from './components/Login.vue'

import { provide, ref } from 'vue'

const fieldSelected = ref('common')

provide('field/selected', fieldSelected)
provide('field/@select', name => fieldSelected.value = name)
</script>

<template>
  <Login />
</template>

<style lang="scss">
html,
body {
  width: 100%;
  height: 100%;
  margin: 0px;
  padding: 0px;
  background: linear-gradient(red, blue);
  overflow: hidden;
  display: flex;
  flex-direction: row;
  justify-content: stretch;
  align-items: stretch;
}

#app {
  flex-grow: 1;
  display: flex;
  flex-direction: row;
  justify-content: stretch;
  align-items: stretch;
  overflow: hidden;
}
</style>
