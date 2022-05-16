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

    <div class="btn-group">
        <button class="btn primary">Borrar</button>
        <button class="btn primary outline">Cancelar</button>
    </div>

    </div>
  </div>
</template>

<style scoped>
/* General */
.dialog {
  width: 481px;
  height: 314px;
  border-radius: 8px;
  box-shadow: 0px 0px 4px 1px;  

  font-family: 'Montserrat';
  font-style: normal;
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
  top: 12px;
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
  color: #FFD912;
  font-size: 2em;
}

.title {
    text-align: center;
}
.title p{
    font-family: 'Roboto';
    font-style: normal;
}

.btn{    
    cursor: pointer;
    padding: 10px 20px 10px 20px;
    border-radius: 8px;    
}

.btn.primary{
    background: #6E41E2;
    border: 1px solid #6E41E2;
    color: white;
}
.btn.primary.outline{
    background: transparent;
    border: 1px solid #6E41E2;
    color: #6E41E2;
}
.btn-group{
    display: flex;
    gap: 1em;
}
</style>