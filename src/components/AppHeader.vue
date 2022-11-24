<script>
    export default {
        name: 'AppHeader',
        data(){
            return{
                menuLinks: [
                    {
                        linkName: 'CHARACTERS',
                    },
                    {
                        linkName: 'COMICS',
                    },
                    {
                        linkName: 'MOVIES',
                    },
                    {
                        linkName: 'TV',
                    },
                    {
                        linkName: 'GAMES',
                    },
                    {
                        linkName: 'COLLECTIBLES',
                    },
                    {
                        linkName: 'VIDEOS',
                    },
                    {
                        linkName: 'FANS',
                    },
                    {
                        linkName: 'NEWS',
                    },
                    {
                        linkName: 'SHOP',
                    }
                ]
            }
        }
    }
</script>

<template>
    <header class="container">
        <div class="header__logo">
            <a href="#">
                <img src="../assets/dc-logo.png" alt="logo-DC">
            </a>
        </div>
        <nav class="header__nav">
            <ul>
                <li v-for="link in menuLinks"><a href="#">{{link.linkName}}</a></li>
            </ul>
        </nav>
    </header>
</template>

<style lang="scss" scoped>
    header {
        display: flex;
        justify-content: space-between;

        & .header__logo img{
            max-width: 4.375rem;
            margin: .9375rem 0;
        }
        & .header__nav ul{
            height: 100%;
            display: flex;
            align-items: center;
            list-style: none;
        }
        & .header__nav ul li{
            margin-left: 1.5625rem;
        }
        & .header__nav ul li a{
            color: black;
            text-decoration: none;
            font-weight: 500;
            font-size: .8125rem;
        }
    }
</style>
