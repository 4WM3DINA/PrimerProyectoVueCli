<template>
  <div id="app">
    <div class="container">
      <h1 class="fw-bold">Tabla de Usuarios</h1>
      <table class="table">
        <thead>
          <tr class="table-danger">
            <th scope="col">#</th>
            <th scope="col">Nombre</th>
            <th scope="col">Apellido</th>
            <th scope="col">Run</th>
            <th scope="col">Fecha de Nacimiento</th>
            <th scope="col">Edad</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(item, index) in personas" :key="index">
            <th scope="row" class="table-dark">{{ index }}</th>
            <td class="table-warning">{{ item.nombre }}</td>
            <td class="table-success">{{ item.apellido }}</td>
            <td class="table-info">{{ item.run }}</td>
            <td class="table-secondary">{{ item.nacimiento }}</td>
            <td class="table-primary">{{ item.edad }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      personas: [
        {
          nombre: "Juan",
          apellido: "Martinez",
          run: "12896756-5",
          nacimiento: "04-04-1998",
          edad: "23",
        },
        {
          nombre: "Luis",
          apellido: "Perez",
          run: "11896523-1",
          nacimiento: "11-07-1986",
          edad: "40",
        },
        {
          nombre: "Ana",
          apellido: "Lopez",
          run: "11852963-7",
          nacimiento: "05-10-1996",
          edad: "26",
        },
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
