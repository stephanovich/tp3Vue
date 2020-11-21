<template>
  <div>
    <h1>questão 3</h1>
    <div class="flex">
      <div>
      <input type="text" id="input-1" class="input" placeholder="Digite a mensagem" v-on:change="mudaTexto($event)">
      </div>
      <div>
      <input type="text" id="input0" class="input" placeholder="Digite uma cor em Hexadecimal" v-on:change="mudaCorText($event)">
      </div>
      <div>
      <input type="number" id="input1" class="input" placeholder="Digite um tamanho em pixels" v-on:change="mudaTamanho($event)">
      </div>
    </div>
    <EditaTexto :myStyle="text">{{texto}}</EditaTexto>
    <hr>
    <h1>Questão 4</h1>
    <div>
      <input type="text" id="inpu2t" class="input" placeholder="Digite uma cor em Hexadecimal" v-on:change="mudaCorQuadrado($event)">
    </div>
    <DesenhaQuadrado :myStyle="cor"/>
  </div>
</template>

<script>
import DesenhaQuadrado from './components/DesenhaQuadrado.vue'
import EditaTexto from './components/EditaTexto.vue'

export default {
  name: 'App',
  components: {
    DesenhaQuadrado,
    EditaTexto
  },
  data(){
    return{
      cor: {
        backgroundColor: "red"
      },
      text:{
        color: "black",
        fontSize: "30px"
      },
      texto: "Um texto"
    }
  },
  methods:{
    mudaCorQuadrado: function(cor){
      this.cor.backgroundColor = cor.target.value
    },
    mudaCorText: function(cor){
      this.text.color = cor.target.value
    },
    mudaTamanho: function(tam){
      this.text.fontSize = tam.target.value + "px"
    },
    mudaTexto: function(msg){
      this.texto = msg.target.value
    }
  },
}
</script>

<style>
.input{
  width: 200px;
  margin-bottom: 20px;
}
.flex{
  display: inline;
}
</style>
