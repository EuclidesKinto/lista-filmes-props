<template>
  <div class="row">

    <!-- coluna 1 -->
    <div class="col-8">
      <h2>Filmes</h2>
      <div class="list-group list-group-flush">
        <FilmesListaIten v-for="(filme, i) in filmes" :key="i" :filmeTitulo="filme"/>
      </div>
    </div>
    <!-- coluna 2 -->
    <div class="col-4">
      <FilmesListaItenInfo/>
    </div>
  </div>
</template>

<script>
import FilmesListaIten from './FilmesListaIten.vue'
import FilmesListaItenInfo from './FilmesListaItenInfo.vue'

export default {
  components: {
    FilmesListaIten,
    FilmesListaItenInfo
  },
  data() {
    return {
      filmes:[
        'Vingadores: Guerra Infinita 1',
        'Vingadores: Guerra Infinita 2',
        'Vingadores: Guerra Infinita 3',

      ]
    }
  },
}
</script>
