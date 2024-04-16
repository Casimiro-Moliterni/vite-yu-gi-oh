<script>
 export default{
  name:'SingleCard'
}
</script>

<template>
    <div class="single-card">
         <div class="image">
            <img src="https://images.ygoprodeck.com/images/cards_small/34541863.jpg" alt="">
         </div>
         <div class="name white">nome</div>
         <div class="archtype">Archetype</div>
    </div>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *; 
  
  .single-card{
    text-align: center;
    background-color:$brand_primary;
    width:calc((100% / 5) - 20px) ;
    margin: 10px;
    .name,
    .archtype{
      padding: 10px 0;

    }
    .white{
      color:white;
    }
  }
</style>