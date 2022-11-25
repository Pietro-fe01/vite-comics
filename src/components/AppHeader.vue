<script>
    export default {
        name: 'AppHeader',
        data(){
            return{
                menuLinks: [
                    {
                        href: '#',
                        label: 'CHARACTERS',
                        active: false,
                    },
                    {
                        href: '#',
                        label: 'COMICS',
                        active: false,
                    },
                    {
                        href: '#',
                        label: 'MOVIES',
                        active: false,
                    },
                    {
                        href: '#',
                        label: 'TV',
                        active: false,
                    },
                    {
                        href: '#',
                        label: 'GAMES',
                        active: false,
                    },
                    {
                        href: '#',
                        label: 'COLLECTIBLES',
                        active: false,
                    },
                    {
                        href: '#',
                        label: 'VIDEOS',
                        active: false,
                    },
                    {
                        href: '#',
                        label: 'FANS',
                        active: false,
                    },
                    {
                        href: '#',
                        label: 'NEWS',
                        active: false,
                    },
                    {
                        href: '#',
                        label: 'SHOP',
                        active: false,
                    }
                ],
            }
        },
        methods: {
            selectMenu: function(index){
                for(let i=0; i<this.menuLinks.length; i++){
                    if(index === i){
                        this.menuLinks[index].active = true;
                    } else {
                        this.menuLinks[i].active = false;
                    }
                }
            }
        },
        mounted(){
            this.menuLinks[1].active = true;
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
                <li @click="selectMenu(index)" v-for="(link, index) in menuLinks"><a :class="{active : link.active}" :href="link.href">{{link.label}}</a></li>
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
            position: relative;
        }
        & .header__nav ul li a{
            color: var(--nav-link-color);
            text-decoration: none;
            font-weight: 600;
            font-size: .8125rem;
        }
    }

    /*--------------------
        ACTIVE LINK MENU
    ---------------------*/
    .active{
        color: #0282f9 !important;
    }
    .active::after{
        content: "";
        display: inline-block;
        width: 100%;
        height: 4px;
        background-color: #0282f9;
        position: absolute;
        bottom: -42px;
        left: 0;
    }
</style>
