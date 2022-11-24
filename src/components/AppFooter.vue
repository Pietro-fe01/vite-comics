<script>
    export default {
        name: 'AppFooter',
    }
</script>

<template>
    <div class="main-footer">
        <div class=main-footer__left>
            <div>
                <h3>DC COMICS</h3>
                <nav>
                    <ul>
                        <li><a href="#"><small>Characters</small></a></li>
                        <li><a href="#"><small>Comics</small></a></li>
                        <li><a href="#"><small>Movies</small></a></li>
                        <li><a href="#"><small>TV</small></a></li>
                        <li><a href="#"><small>Games</small></a></li>
                        <li><a href="#"><small>Videos</small></a></li>
                        <li><a href="#"><small>News</small></a></li>
                    </ul>
                </nav>
            </div>

            <div>
                <h3>SHOP</h3>
                <nav>
                    <ul>
                        <li><a href="#"><small>Shop DC</small></a></li>
                        <li><a href="#"><small>Shop DC Collectibles</small></a></li>
                    </ul>
                </nav>
            </div>
        </div>

        <div class=main-footer__middle>
            <h3>DC COMICS</h3>
            <nav>
                <ul>
                    <li><a href="#"><small>Terms Of Use</small></a></li>
                    <li><a href="#"><small>Privacy policy (New)</small></a></li>
                    <li><a href="#"><small>Ad Choices</small></a></li>
                    <li><a href="#"><small>Advertising</small></a></li>
                    <li><a href="#"><small>Jobs</small></a></li>
                    <li><a href="#"><small>Subscriptions</small></a></li>
                    <li><a href="#"><small>Talent Workshops</small></a></li>
                    <li><a href="#"><small>CPSC Certificates</small></a></li>
                    <li><a href="#"><small>Ratings</small></a></li>
                    <li><a href="#"><small>Shop Help</small></a></li>
                    <li><a href="#"><small>Contact Us</small></a></li>

                </ul>
            </nav>
        </div>

        <div class=main-footer__right>
            <h3>DC COMICS</h3>
            <nav>
                <ul>
                    <li><a href="#"><small>DC</small></a></li>
                    <li><a href="#"><small>MAD Magazine</small></a></li>
                    <li><a href="#"><small>DC Kids</small></a></li>
                    <li><a href="#"><small>DC Universe</small></a></li>
                    <li><a href="#"><small>DC Power Visa</small></a></li>
                </ul>
            </nav>
        </div>

        <div class="bg-image">
        </div>
    </div>

    <div class="bottom-footer">
        ciao
    </div>
</template>

<style lang="scss" scoped>
    .main-footer{
        background-image: url('../assets/footer-bg.jpg');
        background-size: cover;
        display: flex;
        padding: 0 6.25rem;
        padding-top: 2.1875rem;
        padding-bottom: 2.5rem;
        position: relative;
        z-index: -1;

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
        height: 100px;
        width: 100%;
        background-color: var(--bg-footer-bottom-color);
    }
</style>