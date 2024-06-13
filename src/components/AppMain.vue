<script >
import MainSelect from './MainSelect.vue';
import MainCardsList from './MainCardsList.vue';
import MainLoader from './MainLoader.vue';
import axios from 'axios';
import { store } from '../store.js';

export default {
  components:{
    MainSelect,
    MainCardsList,
    MainLoader
  },
  data(){
    return{
        store,
        loader: false,
    }
  },
  methods:{
    getcards(){
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
            .then( (response)=> {
              // handle success
            console.log(response.data.data);
            this.store.cards = response.data.data;
            })
            .catch(function (error) {
             // handle error
            console.log(error);
            })
            .finally(function () {
             // always executed
            });
    },
    getOptions(){
      axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
            .then( (response)=> {
              // handle success
            console.log(response.data);
            this.store.options = response.data;
            })
            .catch(function (error) {
             // handle error
            console.log(error);
            })
            .finally(function () {
             // always executed
            });
    },
    loadInThreeSec(){
      setTimeout(() =>{
        this.loader=true;
      },3000)
    }
    },
    created(){
        this.getcards(),
        this.getOptions(),
        this.loadInThreeSec()
  }
}
</script>

<template>

<main>

  <MainSelect />
  <MainCardsList v-if="loader"/>
  <MainLoader v-else/>

</main>
  
</template>

<style scoped>

</style>