<script >
import MainCard from './MainCard.vue';
import { store } from '../store.js'

export default{
  components:{
    MainCard
  },
  data(){
    return{
      store
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
   <section class="cards-list container">

    <div class="row">

      <h5 class="col-12 p-3 mb-0 bg-black text-white">
        Found 39 cards
      </h5>
      
      <div class="col-12 bg-white ">
        <div class="row">
           
          <MainCard  class="col-3" v-for="card in store.cards" 
          :key="card.id" :card="card"/>
             
        </div>
        
      </div>
      

    </div>

   </section>


  
</template>

<style scoped>

</style>