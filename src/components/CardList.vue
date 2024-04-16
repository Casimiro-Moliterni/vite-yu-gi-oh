<script>
import SingleCard from './SingleCard.vue';
import {store} from '../store.js';
export default{
    name:'CardList',
    components:{
        SingleCard
    },
    data(){
        return{
            store
        }
    }
}
</script>

<template>
    <section class="card-list">
        <div class="container">
           <div class="wrapper-card">
                <SingleCard v-for="card in store.cards" :key="card.id" :cardInfo="card"></SingleCard>
           </div>
        </div>
    </section>
</template>

<style scoped lang="scss"> 
@use '../style/partials/variables' as *; 
.card-list{
    background-color: $brand_primary;
    padding: 20px 0;
      .container{
        background-color: white;
        padding: 20px;
        .wrapper-card{
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
      }
      }
}
</style>