<script setup>

import Dialog from "./components/Dialog.vue";

</script>

<template>
  <main>

    <div class="buttons">
      <button class="btn warning">Abrir warning</button>
      <button class="btn succes">Abrir Succes</button>
      <button class="btn error">Abrir Error</button>
    </div>
    <br>
    <Dialog/>

  </main>
</template>

<style>
/* Importamos la tipografia Montserrat */
@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
/* Importamos la tipografia Roboto */
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap');
</style>
