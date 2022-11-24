<script>
    export default {
        name: 'AppDcBar',
        data(){
            return{
                cardsList: [
                    {
                        img: 'buy-comics-digital-comics.png',
                        cardName: 'DIGITAL COMICS',
                    },
                    {
                        img: 'buy-comics-merchandise.png',
                        cardName: 'DC MERCHANDISE',
                    },
                    {
                        img: 'buy-comics-subscriptions.png',
                        cardName: 'SUBSCRIPTION',
                    },
                    {
                        img: 'buy-comics-shop-locator.png',
                        cardName: 'COMIC SHOP LOCATOR',
                    },
                    {
                        img: 'buy-dc-power-visa.svg',
                        cardName: 'DC POWER VISA',
                    },
                ]
            }
        }
    }
</script>

<template>
    <div class="pre-footer">
        <div class="cards container-small">
            <div class="card" v-for="card in cardsList">
                <a href="#" class="card__info">
                    <img :src="`src/assets/${card.img}`" alt="digital.comics-img">
                    <p>{{card.cardName}}</p>
                </a>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    .pre-footer{
        background-color: var(--bg-pre-footer-color);
        padding: 3.125rem 0;
        & .cards{
            display: flex;
            justify-content: space-between;
            align-items: center;
            & .card:nth-child(4) img{
                width: 1.875rem;
            }
            & .card__info{
                display: flex;
                justify-content: center;
                align-items: center;
                color: white;
                text-decoration: none;

                & img{
                    width: 2.5rem;
                    margin-right: .625rem;
                }
            }
        }
    }
</style>