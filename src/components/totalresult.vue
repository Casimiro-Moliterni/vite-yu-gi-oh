<script>
import {store} from '../store.js';
export default{
    name:'totalresult',
    data(){
        return{
            store
        }
    }
}
</script>
<template>
    <div>carte trovate {{ store.cards.length }}</div>
</template>
<style scoped lang="scss">
div{
    font-size: 20px;
    background: black;
    color: white;
    padding: 20px;
    margin: -10px 10px;
    font-weight: 700;
}

</style>