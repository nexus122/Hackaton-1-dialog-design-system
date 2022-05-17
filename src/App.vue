<script setup>
import DialogComponent from "./components/DialogComponent.vue";
</script>

<script>
export default {
  name: "App",
  components: {
    DialogComponent,
  },
  data() {
    return {
        warning: {
          name: "warning",
          visible: false,
          icon: '<i class="fa-solid fa-exclamation"></i>',
          background_color: 'rgba(255, 217, 18, 0.12)',
          color: '#FFD912',
          title: '¡Cuidado!',
          text: 'No podrás volver atrás',
          buttons: `
          <div class="btn-group">
            <button ref="button" class="btn primary">Borrar</button>
            <button ref="button" class="btn primary outline">Cancelar</button>
          </div>`
        },
        succes: {
          name: 'succes',
          visible:false,
          icon: '<i class="fa-solid fa-check"></i>',
          background_color: 'rgba(39, 174, 96, 0.12)',
          color: 'rgba(39, 174, 96, 1)',
          title: '¡Bien hecho!',
          text: 'Todo ha ido bien 😄',
          buttons: `
          <div class="btn-group">
            <button class="btn primary"> Cerrar Pestaña</button>
          </div>
          `          
        },
        error:{
          name: 'error',
          visible:false,
          icon: '<i class="fa-solid fa-times"></i>',
          background_color: 'rgba(192, 57, 43, 0.12)',
          color: 'rgba(192, 57, 43, 1)',
          title: '¡Error!',
          text: 'Algo ha ido mal 😭',
          buttons: ``
        },        
    };
  },
  methods: {
    showDialog(type) {
      this[type].visible = true;
    },
    closeModal(type) {
      this[type].visible = false;
    }
  },  
}
</script>

<template>
  <main>

    <div class="buttons">
      <button class="btn primary outline" @click="showDialog('warning')">Mostrar warning</button>
      <button class="btn primary outline" @click="showDialog('succes')">Mostrar succes</button>
      <button class="btn primary outline" @click="showDialog('error')">Mostrar error</button>
    </div>
    
    <DialogComponent @close="closeModal($event)" :dialogInfo="warning"/>
    <DialogComponent @close="closeModal($event)" :dialogInfo="succes"/>
    <DialogComponent @close="closeModal($event)" :dialogInfo="error"/>

  </main>
</template>

<style>
/* Importamos la tipografia Montserrat */
@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
/* Importamos la tipografia Roboto */
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap');

main{
  display:flex;
  flex-direction:column;
  align-items: center;
}

.buttons {
  display: flex;    
  margin-bottom: 1em;
  margin-top: 1em;
  gap: 1em;
}

/* Buttons de Dialogs */

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
