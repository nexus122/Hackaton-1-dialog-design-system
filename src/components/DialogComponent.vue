<template>
  <div class="dialog" v-if="dialogInfo.visible">
    <!-- BTN CLOSE -->
    <div class="close">
      <i class="fa-solid fa-xmark"></i>
    </div>
    <!-- Contenido del popup -->
    <div class="popUpContent">
      <!-- Dialog icon -->
      <div class="icon" :style="{color:dialogInfo.color, background: dialogInfo.background_color}">
        <span class="icono" v-html="dialogInfo.icon"></span>
      </div>
      <!-- Title and text -->
      <div class="title">
        <h1>{{dialogInfo.title}}</h1>
        <p>{{dialogInfo.text}}</p>
      </div>

      <div v-html="dialogInfo.buttons"></div>
      
    </div>
  </div>
</template>

<script>
export default {
  name: "DialogComponent",
  emits: ['close'],
  props: {
    dialogInfo: {
      type: Object,
      required: true
    }
  }
}
</script>


<style scoped>
/* General */
.dialog {
  width: 481px;
  height: 314px;
  border-radius: 8px;
  
  box-shadow: 0px 4px 4px rgba(51, 51, 51, 0.04), 0px 4px 16px rgba(51, 51, 51, 0.08);

  font-family: "Montserrat";
  font-style: normal;
}

/* Contenido del popup */
.popUpContent {
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
  right: 0px;
  top: 0px;
  border-radius: 100%;

  /* Colors / Star */
  /*background: rgba(255, 217, 18, 0.12);*/

}

.icono {
  /* 56px / Attention */
  /*color: #FFD912;*/
  font-size: 2em;
}

.title {
  text-align: center;
}
.title p {
  font-family: "Roboto";
  font-style: normal;
  margin-top: 8px;
}

.btn-group {
  display: flex;
  gap: 1em;
}

.btn {
  cursor: pointer;
  padding: 10px 20px 10px 20px;
  border-radius: 8px;
  min-width: 44px;  
}

.btn.primary {
  background: #6e41e2;
  border: 1px solid #6e41e2;
  color: white;
}

.btn.primary.outline {
  background: transparent;
  border: 1px solid #6e41e2;
  color: #6e41e2;
}

</style>