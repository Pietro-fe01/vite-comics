<script>
    export default {
        name: 'AppFooter',
    }
</script>

<template>
    <div class="main-footer">
        <div class="container">
            <div class=main-footer__left>
                <div>
                    <h3>DC COMICS</h3>
                    <nav>
                        <ul>
                            <li><a href="#">Characters</a></li>
                            <li><a href="#">Comics</a></li>
                            <li><a href="#">Movies</a></li>
                            <li><a href="#">TV</a></li>
                            <li><a href="#">Games</a></li>
                            <li><a href="#">Videos</a></li>
                            <li><a href="#">News</a></li>
                        </ul>
                    </nav>
                </div>

                <div>
                    <h3>SHOP</h3>
                    <nav>
                        <ul>
                            <li><a href="#">Shop DC</a></li>
                            <li><a href="#">Shop DC Collectibles</a></li>
                        </ul>
                    </nav>
                </div>
            </div>

            <div class=main-footer__middle>
                <h3>DC COMICS</h3>
                <nav>
                    <ul>
                        <li><a href="#">Terms Of Use</a></li>
                        <li><a href="#">Privacy policy (New)</a></li>
                        <li><a href="#">Ad Choices</a></li>
                        <li><a href="#">Advertising</a></li>
                        <li><a href="#">Jobs</a></li>
                        <li><a href="#">Subscriptions</a></li>
                        <li><a href="#">Talent Workshops</a></li>
                        <li><a href="#">CPSC Certificates</a></li>
                        <li><a href="#">Ratings</a></li>
                        <li><a href="#">Shop Help</a></li>
                        <li><a href="#">Contact Us</a></li>

                    </ul>
                </nav>
            </div>

            <div class=main-footer__right>
                <h3>DC COMICS</h3>
                <nav>
                    <ul>
                        <li><a href="#">DC</a></li>
                        <li><a href="#">MAD Magazine</a></li>
                        <li><a href="#">DC Kids</a></li>
                        <li><a href="#">DC Universe</a></li>
                        <li><a href="#">DC Power Visa</a></li>
                    </ul>
                </nav>
            </div>
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
        z-index: -1;

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