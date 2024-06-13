<script >


export default{
  
  data(){
    return{
      
    }
  },
  props:{
    card:{
      type: Array,
      required:true
    }
  }
}
</script>

<template>

<article class="card  mb-3">
  <img :src="card.card_images[0].image_url" class="card-img-top" alt="card">
  <div class="card-body">
    <h6 class="card-title">

      {{ card.name }}

    </h6>
    <p class="card-text">

      {{ card.archetype }}

    </p>
  </div>
</article>


  
</template>

<style scoped>

article{}

</style>