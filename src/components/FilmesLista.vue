<template>
  <div class="row">

    <!-- coluna 1 -->
    <div class="col-8">
      <h2>Filmes</h2>
      <ul class="list-group list-group-flush">
        <FilmesListaIten v-for="filme in filmes" 
        :key="filme.id" 
        :filme="filme"
        />
      </ul>
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
        {id: 1, titulo: "Vingadores: Guerra Infinita 1", ano: 2020},
        {id: 2, titulo: "Vingadores: Guerra Infinita 2", ano: 2020},
        {id: 3, titulo: "Vingadores: Guerra Infinita 3", ano: 2020},
        {id: 4, titulo: "Vingadores: Guerra Infinita 4", ano: 2020},
      ]
    }
  },
}
</script>
