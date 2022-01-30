<template>
  <section>
    <div id="aside">
      <a @click="cambiarFoto(1)">
        <img v-bind:src="fotos[1]" alt="imagen de producto" copyright="c-by ErikaA" />
      </a>
      <a @click="cambiarFoto(2)">
        <img v-bind:src="fotos[2]" alt="imagen de producto" copyright="c-by ErikaA" />
      </a>
      <a @click="cambiarFoto(3)">
        <img v-bind:src="fotos[3]" alt="imagen de producto" copyright="c-by ErikaA" />
      </a>
    </div>
    <div id="principal">
      <img v-bind:src="fotos[0]" alt="imagen de producto" copyright="c-by ErikaA" />
    </div>
  </section>
</template>

<script>
export default {
  Name: "ImagenProducto",
  data() {
    return {
      fotos: [
        require("../assets/imagen1.jpg"),
        require("../assets/imagen1.jpg"),
        require("../assets/imagen2.jpg"),
        require("../assets/imagen3.jpg"),
      ],
    };
  },
  methods: {
    cambiarFoto(id) {
      this.fotos[0] = this.fotos[id];
    },
  },
};
</script>

<style scoped>
section {
  display: flex;
  cursor: pointer;
}
#aside {
  display: flex;
  flex-direction: column;
}
#aside img {
  width: 200px;
  height: 200px;
  margin: 10px;
  border-radius: 14px;
}
#principal img {
  width: 650px;
  height: 650px;
  margin: 10px;
  border-radius: 25px;
}
</style>