<script>
export default {
    name:'AppHeader'
}
</script>

<template>
    <header>
        <div class="image">
            <img src="https://vignette1.wikia.nocookie.net/yugiohenespanol/images/a/aa/Yugioh_anime_logo.jpg/revision/latest?cb=20130310042737&path-prefix=es" alt="">
        </div>
        <h1>Yu-Gi-Oh API</h1>
    </header>
</template>

<style scoped lang="scss">
header{
    padding: 15px 20px;
    display: flex;
    align-items: center;

    .image{
        width: 50px;
        margin-right: 20px;
    }
}
</style>