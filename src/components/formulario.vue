<template>
  <div class="formulario">
    <h2>Registro de Usuario</h2>
    <form @submit.prevent="registrarUsuario">
      <label>Nombre:</label>
      <input type="text" v-model="nombre" />

      <label>Dirección:</label>
      <input type="text" v-model="direccion" />

      <label>Edad:</label>
      <input type="number" v-model="edad" />

      <button type="submit">Registrar</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "Formulario",
  data() {
    return {
      nombre: "",
      direccion: "",
      edad: null,
    };
  },
  methods: {
    registrarUsuario() {
      console.log("Usuario registrado:", this.nombre, this.direccion, this.edad);
      alert("Usuario registrado con éxito");
    },
  },
};
</script>

<style scoped>
.formulario {
  max-width: 400px;
  margin: 0 auto;
}
label {
  display: block;
  margin-top: 10px;
}
input {
  width: 100%;
  padding: 5px;
  margin-top: 5px;
}
button {
  margin-top: 15px;
  padding: 8px 12px;
}
</style>
