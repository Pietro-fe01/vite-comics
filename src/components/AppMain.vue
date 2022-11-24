<script>
    export default {
        name: 'AppMain',
    }
</script>

<template>
    <main>
        <div class="jumbotron"></div>
    </main>
</template>

<style lang="scss" scoped>
    main {
        background-color: var(--bg-main-color);
        color: white;
        background-image: url('../assets/jumbotron.jpg');
        background-size: cover;
        height: 560px;
    }
</style>