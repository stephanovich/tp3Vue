<template>
<div class="flex">
  <div class="cubo" id="cubo" :style="myStyle">
  </div>
</div>
</template>

<script>
export default {
  name: 'DesenhaQuadrado',
  props: {
    myStyle:{
      backgroundColor: String
    },
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.cubo{
  width: 400px;
  height: 400px;
  color: black;
  background-color: #000;
  border: 1px solid black;
  margin-right: 20px;
}
.flex{
  display: flex;
}

</style>
