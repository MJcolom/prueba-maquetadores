<template>
  <div>
    <Portada :menu="menu" />
    <Proyectos />
    <Promociones />
    <Contacto />
  </div>
  
</template>

<script>
export default {
  data() {
    return {
      menu: [
        {
          nombre: "Quienes somos",
          url: ""
        },
        {
          nombre: "Proyectos",
          url: ""
        },
        {
          nombre: "Promociones",
          url: ""
        },
        {
          nombre: "Contacto",
          url: ""
        },
      ]
    }
  },
}
</script>
<style>
  .cover:before {
    content: "";
    display: block;
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    width: auto;
    height: auto;
    background: #848993;
    opacity: 0.3;
}
</style>