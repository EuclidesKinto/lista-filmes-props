<template>
    <li class="list-group-item">
        <span>{{ filmeTituloConcatenado }} | {{ filmeLancamento }}</span>
        <button class="btn btn-success float-right">Editar</button>
    </li>
</template>
<script>
export default {
    props: {
      titulo: {
        type: String,
        required: true,
        default: 'Filme padrão'
      },
      ano:{
          type: Number,
          required: true
      }
    },
    computed:{
        filmeTituloConcatenado(){
            return `Titulo: ${this.titulo}`
        },
        filmeLancamento(){
            return `Lançamento: ${this.ano}`
        }
    }
}
</script>
