<template>
    <footer class="footer">
        <div class="container">
            <div class="footer-wrapper">
                <div class="footer-logo">
                    <img src="../../assets/images/logo_seo_2x.png" alt="AvadaSEO footer logo" class="logo">
                </div>
                <div class="footer-menu">
                    <nav class="footer-nav">
                        <ul class="list">
                            <li class="item" v-for="(link, index) in links" :key="index">
                                <a class="link" :class="{'selected' : link.selected}" :href="link.link" :title="link.name">
                                    {{link.name}}
                                </a>
                            </li>
                        </ul>
                    </nav>
                </div>
                <div class="footer-copyright">
                    <p>© Copyright 2012 - 2020   |   Avada Theme by <a class="link" href="#">ThemeFusion</a>   |   All Rights Reserved   |   Powered by <a class="link" href="#">WordPress</a></p>
                </div>
                <div class="footer-socials">
                    <div class="icon">
                        <i class="fab fa-facebook-f"></i>
                    </div>
                    <div class="icon">
                        <i class="fab fa-instagram"></i>
                    </div>
                    <div class="icon">
                        <i class="fab fa-twitter"></i>
                    </div>
                    <div class="icon">
                        <i class="fab fa-youtube"></i>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer',
    props: {
        links: Array
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/partials/variables.scss';
.footer {
    .footer-wrapper {
        display: flex;
        flex-direction: column;
        align-items: center;
        padding: 70px 0;
    }
    &-logo {
        height: 50px;
        .logo {
            height: 100%;
        }
    }
    &-nav {
        padding: 3rem 0;
        .list {
            display: flex;
            align-items: center;
            .item {
                margin: 0 1rem;
                .link {
                    color: $Scorpion;
                    &.selected, &:hover {
                        color: $Yellow_Orange;
                    }
                }
            }
        }
    }
    &-copyright {
        color: $Regent_Gray;
        .link {
            color: $Yellow_Orange;
        }
    }
    &-socials {
        display: flex;
        align-items: center;
        font-size: 1.4rem;
        color: $Scorpion;
        margin-top: 2rem;
        .icon {
            margin: 0 .7rem;
        }
    }
}
</style>