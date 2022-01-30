<template>
  <section>
    <h1>Pamela buntal azul</h1>
    <h2>150€ IVA incluido</h2>
    <div>
      <button
        class="contador"
        @click="cambiarContador('-1')"
        type="button"
        name="button"
      >
        -
      </button>
      <input type="text" name="number" :value="contador" />
      <button
        class="contador"
        @click="cambiarContador('1')"
        type="button"
        name="button"
      >
        +
      </button>
    </div>
    <br />
    <div>
      <button id="carrito">
        <i class="fas fa-shopping-cart"></i>
        <span>AÑADIR CARRITO</span>
      </button>
    </div>
  </section>
</template>

<script>
export default {
  Name: "DatosProducto",
  data() {
    return {
      contador: 1,
    };
  },
  methods: {
    cambiarContador(num) {
      this.contador += parseInt(num);
      if (!isNaN(this.contador) && this.contador < 0) {
        this.contador = 0;
      }
    },
  },
};
</script>

<style scoped>
section {
  flex-direction: column;
  margin-left: 50px;
  justify-content: flex-start;
  display: flex;
  
}
h1,
h2,
div {
  font-family: monospace;
  text-align: center;
}
h1 {
  font-size: 37px;
  margin-top: 5px;
}
input {
  width: 20px;
  height: 20px;
  text-align: center;
  font-size: medium;
  font-weight: bold;
}
.contador {
  width: 26px;
  height: 26px;
  text-align: center;
}
button {
  background-color: rgb(168, 167, 167);
  color: white;
  font-family: monospace;
  margin: 0;
  cursor: pointer;
  font-weight: bold;
  
}
i{
  margin-right: 10px;
  color: rgb(219, 89, 219);
}
#carrito{
  padding: 7px;
}
</style>