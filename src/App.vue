<script>
import axios from 'axios';
import { store } from './store.js';
import AppHeader from './components/AppHeader.vue';
import CardList from './components/CardList.vue';

export default{
  components:{
       AppHeader,
       CardList
  },
  data(){
    return{
      store
    };
  },
  methods:{
     generateApi(){
      const queryParams = {
        num : 20,
        offset: 0
      };
         axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php', {
          params:queryParams
         })
         .then((response)=>{
         store.cards= response.data.data;
         })
     }
  },
  mounted(){
    this.generateApi()
  }
}
</script>

<template>
 <AppHeader></AppHeader>
 <main>
<CardList></CardList>
 </main>
</template>

<style lang="scss">
@use './style/generic';
</style>