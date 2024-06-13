<script >
import { store } from '../store';



export default{
  
  data(){
    return{
      store,

    }
  }
}
</script>

<template>
<div class="container">
  <div class="row col-2">

   <select class="form-select mb-4 " aria-label="select">
      <option v-for="option in store.options" 
      :key="option.id" :option="option" >{{ option.archetype_name }}</option>
     
   </select>

  </div>
</div>


</template>

<style scoped lang="scss">

</style>