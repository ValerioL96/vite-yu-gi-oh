<script >
import MainCard from './MainCard.vue';


export default{
  components:{
    MainCard
  },
  data(){
    return{

    }
  }
}
</script>

<template>
   <section class="cards-list container">

    <div class="row">

      <h5 class="col-12 p-3 bg-black text-white">
        Found 39 cards
      </h5>
      <MainCard />

    </div>

   </section>


  
</template>

<style scoped>

</style>