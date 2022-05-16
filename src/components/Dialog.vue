<template>
  <div class="dialog">
    <!-- BTN CLOSE -->
    <div class="close">
      <i class="fa-solid fa-xmark"></i>
    </div>
    <!-- Contenido del popup -->
    <div class="popUpContent">
      <!-- Dialog icon -->
      <div class="icon">
        <i class="fa-solid fa-exclamation"></i>
      </div>
      <!-- Title and text -->
      <div class="title">
        <h1>¡Cuidado!</h1>
        <p>No podras volver atrás</p>
      </div>
    </div>
  </div>
</template>

<style>
/* General */
.dialog {
  width: 481px;
  height: 314px;
  border-radius: 8px;
  box-shadow: 0px 0px 4px 4px;  
}

/* Contenido del popup */
.popUpContent{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

/* BTN cerrar */
.close {
  display: flex;
  justify-content: center;
  align-items: center;

  background: #6e41e2;
  color: white;
  width: 44px;
  height: 44px;

  position: relative;
  left: calc(100% - 44px - 12px);
  top: calc(0 + 44px + 12px);
  border-radius: 100px;

  cursor: pointer;

  font-size: 1.5em;
  box-sizing: border-box;
}

/* Dialog Icon */
.icon {
display: flex;
justify-content: center;
align-items: center;
  width: 96px;
  height: 96px;  
}

.icon i {
  /* 56px / Attention */
  color: yellow;
  font-size: 2em;
}
</style>