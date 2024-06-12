<script >
import { store } from '../store.js'

export default{
  
  data(){
    return{
      store
    }
  }
}
</script>

<template>

<div class="col-12 bg-white p-3">
        <div class="row">
          <article class="col-3" v-for="card in store.cards" 
          :key="card.id" :card="card">
             <div class="card w-150 mb-3">
             <img :src="card.ygoprodeck_url" class="card-img-top" alt="...">
             <div class="card-body">
              <h6 class="card-title">
                {{ card.name }}
              </h6>
               <p class="card-text">
                {{ card.archetype }}
               </p>
             </div>
             </div>
             
          </article>
        </div>
        
      </div>
  
</template>

<style scoped>

</style>