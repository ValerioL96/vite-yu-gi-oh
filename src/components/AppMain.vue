<script >
import MainSelect from './MainSelect.vue';
import MainCardsList from './MainCardsList.vue';
import axios from 'axios';
import { store } from '../store.js';

export default {
  components:{
    MainSelect,
    MainCardsList
  },
  data(){
    return{
        store,
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
    }
    },
    created(){
        this.getcards()
  }
}
</script>

<template>

<main>
    <MainCardsList />
</main>
  
</template>

<style scoped>

</style>