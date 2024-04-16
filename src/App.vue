<script>
import axios from 'axios';
import { store } from './store.js';

export default{
  components:{

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
 {{ store.miavar }}
</template>

<style lang="scss">
@use './style/generic';
</style>