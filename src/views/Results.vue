<template>
  <div class= "bg-dark2">
    <h1>¡Peleador Encontrado!</h1>
    <div>
      <p>{{peleador.id}}</p>
      <p>{{peleador.nombre}}</p>
      <img :src="peleador.imgSrc" alt="">
    </div>
  </div>
</template>
<script>
export default {
  data: ()=>({
   peleador:""
  }), 
  created() {
    const idPeleador= this.$route.params.id
    fetch("/peleadores.json")
      .then((res) => res.json())
      .then((data) => {
        this.peleador = data.find((item)=> (
          item.id == idPeleador
        ));
      });
  },
}
</script>


<style>

.bg-dark2 {
    background-color: #f7a0e1!important;
    font-family: 'Courier New', Courier, monospace;
}

</style>