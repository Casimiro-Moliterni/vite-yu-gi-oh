<script>
import axios from 'axios';
import { store } from './store.js';
import AppHeader from './components/AppHeader.vue';
import CardList from './components/CardList.vue';
import AppFilter from './components/AppFilter.vue';

export default{
  components:{
       AppHeader,
       CardList,
       AppFilter
  },
  data(){
    return{
      store
    };
  },
  methods:{
     generateApiCards(){

      const queryParams = {
        num : 20,
        offset: 0
      };

      if(store.searchedStatus !== ''){
        queryParams.archetype = store.searchedStatus;
      }

         axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php', {
          params:queryParams
         })
         .then((response)=>{
         store.cards= response.data.data;
         })
     }
  },
  mounted(){
    this.generateApiCards()
  }
}
</script>

<template>
 <AppHeader></AppHeader>
 <main>
<AppFilter @searchPerformed="generateApiCards()"></AppFilter>
<CardList></CardList>
 </main>
</template>

<style lang="scss">
@use './style/generic';
</style>