<template>
  <div id="cabecera">
    <Cabecera />
    <Menu />
  </div>

  <div id="container">
    <Breadcrumbs />
    <div id="producto">
      <Articulo />
      <DatosProducto />
    </div>
    <Descripcion />
  </div>
  <Pie />
</template>

<script>
import Breadcrumbs from "./components/Breadcrumbs.vue";
import Cabecera from "./components/Cabecera.vue";
import Menu from "./components/Menu.vue";
import Articulo from "./components/Articulo.vue";
import DatosProducto from "./components/DatosProducto.vue";
import Descripcion from "./components/Descripcion.vue";
import Pie from "./components/Pie.vue";

export default {
  name: "App",
  components: {
    Cabecera,
    Menu,
    Breadcrumbs,
    Articulo,
    DatosProducto,
    Descripcion,
    Pie,
  },
};
</script>

<style>
body {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
}

#app {
  font-family: monospace;
}
.container {
  max-width: 1400px;
  margin: auto;
}

#producto {
  display: flex;
  justify-content: center;
  margin: 1em;
}
#container {
  margin: 0 auto;
  max-width: 1400px;
}
#cabecera{
  display: flex;
  align-items: center;
  width: 100%;
  background-color: rgb(125 125 199);
  align-content: space-around;
}
</style>
