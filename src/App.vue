<template>
  <div id="App">
    <div class="profile" v-for="personaje in personajes" :key="personaje">
      <div class="contenedor">
        <img class="rounded" :src="personaje.src" alt="">
      <p class="texto">{{personaje.nombre}}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",

  data() {
    return {

      
      personajes: [
        {
          nombre: "Rick Sanchez",
          src: "https://rickandmortyapi.com/api/character/avatar/1.jpeg",
        },
        {
          nombre: "Morty Smith",
          src: "https://rickandmortyapi.com/api/character/avatar/2.jpeg",
        },
        {
          nombre: "Beth Smith",
          src: "https://rickandmortyapi.com/api/character/avatar/4.jpeg",
        },
        {
          nombre: "Summer Smith",
          src: "https://rickandmortyapi.com/api/character/avatar/3.jpeg",
        },
        {
          nombre: "Jerry Smith",
          src: "https://rickandmortyapi.com/api/character/avatar/5.jpeg",
        },
      ],
    };
  },
};
</script>

<style>

  body {
  background: url("https://rickandmortypod.com/wp-content/uploads/2018/11/cropped-RM_page-header_background1-3.png") no-repeat center center
    fixed;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
}
  .rounded{
    border-radius: 50%;
    width: 5rem;
  }
  .contenedor{
    display: flex;
    align-items: center;
    padding: 1rem;
  }
  .texto{
    margin-left: 1rem;
    color: white;
  }
</style>
