<script>
import axios from 'axios';
import { store } from '../store.js';
export default{
    name:'AppFilter',
    data() {
        return {
            store,
           archetypes:[]
        };
    },
    methods:{
        getArchetypes(){
         axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
         .then((response)=>{
            this.archetypes=response.data;
         });
        }
    },
    mounted(){
        this.getArchetypes()
    }
}
</script>

<template>
   <section>
      <div class="container">
        <select v-model="store.searchedStatus" @change="$emit('searchPerformed')">
            <option value="">Scegli tipo</option>
            <option v-for="archetype in archetypes" :value="archetype.archetype_name">{{archetype.archetype_name}}</option>
        </select>
      </div>
   </section>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *; 
    
    section{
        background-color: $brand_primary;
        padding-top: 20px; 
        select{
            border: none;
            padding: 10px;
            border-radius: 10px;
            option{
                font-size: 18px;
            }
        }
    }
</style>