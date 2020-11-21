<template>
<div>
    <p class="EditaTexto" :style="myStyle"><slot /></p>
</div>
</template>

<script>
export default {
  name: 'EditaTexto',
  props: {
      msg: String,
      myStyle:{
      color: String,
      size: String,
    },
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
