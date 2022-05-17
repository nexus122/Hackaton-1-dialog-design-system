# Hackaton-1-dialog-design-system
**Primer reto de la Hackaton.**</br>
He escogido Vue porque, ademas de tener mas practica con el, me gustaba el hecho de poder abstraer el componente, y poder mutarlo en el futuro simplemente editando datos.
# User stories
- [x] Task 1 → Que se pueda ver el diseño de los diálogos de warning
- [x] Task 2 → Que se pueda ver el diseño para los diálogos de success
- [x] Task 3 → Que se pueda ver el diseño para los diálogos de error
- [x] Task 4 → Que se pueda ver 3 botones para abrir cada uno de los diálogos y las acciones de cerrar y aceptar son funcionales

## Enlaces de interes:
- [Demo](https://hackaton-1-dialog-design-system.vercel.app/)
- [Figma](https://www.figma.com/file/ETSvclvkfXzUIJjkufXRJ9?node-id=98:14530)

## 📂 Estructura de carpetas
- 📂 node_modules
- 📂 public
  - favicon.ico
- 📂 src
  - 📂 components
    - 📜 DialogComponent.vue
  - 📜 App.vue
  - 📜 main.js
- 📜 .gitignore
- 📜 index.html
- 📜 package-lock.json
- 📜 package.json
- 📜 Readme.md
- 📜 vite.config.js

## Estructura de datos:
Datos que he utilizado en Vue para dibujar los distintos elementos.
```` javascript
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
````

## 📝 Tareas
- [x] Crear un componente DialogComponent
- [x] Crear la información para cada uno de los Dialogs.
- [x] Enviar la información como una prop para hacer dinámico el Dialog.
- [x] Maquetar el Dialog como en Figma, utilizando tamaños, radios, colores, etc...
- [x] Crear una función de cierre que emita al padre cuando se pulsa la X de cerrar el Dialog.
- [x] Recibir evento y modificar los datos para que la visibilidad sea false.
- [x] Crear Botones dinámicos que se envían como datos en la prop
- [ ] Conseguir que cada botón individual cierre el Modal.
  - [x] como alternativa, poner la función de cierre al padre de los botones dinámicos.
