<template>

  <div class="jumbotron">
    <label for="color">Color</label>
    <input type="text" v-model="color">

    <label for="fondo">Fondo</label>
    <input type="text" v-model="fondo">

    <label for="size">Size</label>
    <input type="text" v-model="size">
    <br>
    <br>
    <br>

    <label for="texto" >Texto</label>
    <input type="texto" v-model.trim="texto" :style="{color: color, backgroundColor: fondo, fontSize: size}">
    <hr>
    <p>Cantidad de palabras: {{contar}}</p>
    <br>
    <br>
    <br>

    <table class="table table-dark">
      <tr>
        <th>numero pregunta</th>
        <th>Respuesta</th>
      </tr>
    <tr>
      <td>1</td>
      <td>b</td>
    </tr>
    <tr>
      <td>2</td>
      <td>c</td>
    </tr>
    <tr>
      <td>3</td>
      <td>b</td>
    </tr>
    <tr>
      <td>4</td>
      <td>d</td>
    </tr>   
    <tr>
      <td>5</td>
      <td>d</td>
    </tr>
    </table>
   

  </div>
</template>

<script>

  export default  {
    name: 'src-components-input-texto',
    props: [],
    mounted () {

    },
    data () {
      return {
        texto: "",
        color: "",
        fondo: "",
        size: "",
        
      }
    },
    methods: {
      contador(texto){
        let cant = 0
        if (texto == "") {
          return cant
        }
        cant = texto.split(" ").length
        console.log(cant)
        return cant
      },

    },
    computed: {
      contar: function () {
        return (this.texto.split(" ").length)
      }
    }
    
}


</script>

<style scoped lang="css">
  .src-components-input-texto {

  }

</style>
