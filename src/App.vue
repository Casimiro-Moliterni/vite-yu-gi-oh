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

  },
  mounted(){
    console.log('ciao')
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