<script>
    export default {
        name: 'AppFooter',
        data(){
            return {
                footerLinks: [
                    {
                        title: 'DC COMICS',
                        links: [
                            'Characters',
                            'Comics',
                            'Movies',
                            'TV',
                            'Games',
                            'Videos',
                            'News'
                        ]
                    },
                    {
                        title: 'SHOP',
                        links: [
                            'Shop DC',
                            'Shop DC Collectibles'
                        ]
                    },
                    {
                        title: 'DC',
                        links: [
                            'Terms Of Use',
                            'Privacy policy (New)',
                            'Ad Choices',
                            'Advertising',
                            'Jobs',
                            'Subscriptions',
                            'Talent Workshops',
                            'CPSC Certificates',
                            'Ratings',
                            'Shop Help',
                            'Contact Us',
                        ]
                    },
                    {
                        title: 'SITES',
                        links: [
                            'DC',
                            'MAD Magazine',
                            'DC Kids',
                            'DC Universe',
                            'DC Power Visa'
                        ]
                    }
                ]
            }
        }
    }
</script>

<template>
    <div class="main-footer">
        <div class="container">
            <!-- Menu link footer left -->
            <div class=main-footer__left>
                <div>
                    <h3>{{footerLinks[0].title}}</h3>
                    <nav>
                        <ul>
                            <li v-for="link in footerLinks[0].links"><a href="#">{{link}}</a></li>
                        </ul>
                    </nav>
                </div>

                <div>
                    <h3>{{footerLinks[1].title}}</h3>
                    <nav>
                        <ul>
                            <li v-for="link in footerLinks[1].links"><a href="#">{{link}}</a></li>
                        </ul>
                    </nav>
                </div>
            </div>
            <!-- /Menu link footer left-->

            <!-- Menu link footer middle-->
            <div class=main-footer__middle>
                <h3>{{footerLinks[2].title}}</h3>
                <nav>
                    <ul>
                        <li v-for="link in footerLinks[2].links"><a href="#">{{link}}</a></li>
                    </ul>
                </nav>
            </div>
            <!-- /Menu link footer middle-->

            <!-- Menu link footer right-->
            <div class=main-footer__right>
                <h3>{{footerLinks[3].title}}</h3>
                <nav>
                    <ul>
                        <li v-for="link in footerLinks[3].links"><a href="#">{{link}}</a></li>
                    </ul>
                </nav>
            </div>
            <!-- /Menu link footer right-->

            <div class="bg-image"></div>
        </div>
    </div>

    <div class="bottom-footer">
        <div class="container">
            <div class="sign-up">
                <button>SIGN-UP NOW!</button>
            </div>
            <div class="follow-us">
                <h2>FOLLOW-US</h2>
                <a href="#">
                    <img src="../assets/footer-facebook.png" alt="facebook-img">
                </a>
                <a href="#">
                    <img src="../assets/footer-twitter.png" alt="twitter-img">
                </a>
                <a href="#">
                    <img src="../assets/footer-youtube.png" alt="youtube-img">
                </a>
                <a href="#">
                    <img src="../assets/footer-pinterest.png" alt="pinterest-img">
                </a>
                <a href="#">
                    <img src="../assets/footer-periscope.png" alt="periscope-img">
                </a>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    .main-footer{
        background-image: url('../assets/footer-bg.jpg');
        background-size: cover;
        padding-top: 2.1875rem;
        padding-bottom: 2.5rem;
        position: relative;
        // z-index: -1;

        & .container{
            display: flex;
        }

        &__left nav:first-of-type{
            margin-bottom: 1.25rem;
        }

        &__left, &__middle, &__right{
            margin-right: 2.1875rem;

            & h3{
                color: white;
            }
        }

        & nav ul{
            list-style: none;

            & li a{
                color: #698887;
                text-decoration: none;
                font-size: .875rem;
            }
            
            & a:hover{
                color: rgba($color: #fff, $alpha: 0.8) !important;
            }
        }

        & .bg-image{
            position: absolute;
            top: -45px;
            right: 200px;
            background-image: url('../assets/dc-logo-bg.png');
            background-position: center;
            background-repeat: no-repeat;
            height: 450px;
            width: 570px;
        }   
    }
    .bottom-footer{
        background-color: var(--bg-footer-bottom-color);
        
        & .container{
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.5625rem 0;

            & .sign-up button{
                color: white;
                border: 2.5px solid var(--footer-bottom-color);
                padding: .9375rem .625rem;

                &:hover{
                    background-color: rgba($color: white, $alpha: 0.2);
                    animation: shake 0.1s linear;
                }
                @keyframes shake{
                    0% {
                        transform: rotate(-10deg);
                    }
                    100% {
                        transform: rotate(10deg);
                    }
                }
            }
            
            & .follow-us{
                display: flex;

                & h2{
                    color: var(--footer-bottom-color);
                }

                & img{
                    margin-left: 1.25rem;

                    &:hover{
                        filter: drop-shadow(0 0 4px white);
                    }
                }
            }
        }
    }
</style>