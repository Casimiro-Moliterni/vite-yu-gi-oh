<script>

 export default{
  name:'SingleCard',
  props:{
    cardInfo:Object
  }
}
</script>

<template>
    <div class="single-card">
         <div class="image">
            <img :src="cardInfo.card_images[0].image_url_small" :alt="cardInfo.name">
         </div>
         <h3 class="name white">{{ cardInfo.name }}</h3>
         <div class="archetype" >{{ cardInfo.archetype }}</div>
    </div>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *; 
  
  .single-card{
    text-align: center;
    background-color:$brand_primary;
    width:calc((100% / 5) - 20px) ;
    margin: 10px;
    .image{
       img{
        width: 100%;
        object-fit: cover;
       }
    }
    .name,
    .archetype,
    .image{
     margin-bottom: 10px;

    }
    .white{
      color:white;
    }
    .archetype{
      font-size: 20px;
      font-weight: 700;
    }
  }
</style>