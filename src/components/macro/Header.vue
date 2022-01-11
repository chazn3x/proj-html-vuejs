<template>
    <header class="header">
        <div class="container">
            <div class="header-wrapper">
                <div class="header-logo">
                    <img class="logo" src="../../assets/images/logo_seo_w_2x.png" alt="AvadaSEO small logo">
                </div>
                <div class="header-menu">
                    <nav class="header-nav">
                        <ul class="list">
                            <li class="item" v-for="(link, index) in links" :key="index">
                                <a class="link" :class="{'selected' : link.selected}" :href="link.link" :title="link.name">
                                    {{link.name}}
                                    <div class="apply" v-if="link.apply">Apply</div>
                                </a>
                            </li>
                        </ul>
                        <button class="button">
                            Get in touch now
                        </button>
                    </nav>
                </div>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: 'Header',
    data() {
        return {
            links: [
                {
                    name: 'Home',
                    link: '#',
                    selected: true,
                },
                {
                    name: 'Who We Are',
                    link: '#',
                    selected: false,
                },
                {
                    name: 'What We Do',
                    link: '#',
                    selected: false,
                },
                {
                    name: 'Where We Work',
                    link: '#',
                    selected: false,
                },
                {
                    name: 'Careers',
                    link: '#',
                    selected: false,
                    apply: true
                },
                {
                    name: 'News',
                    link: '#',
                    selected: false,
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/partials/variables.scss';
@import '../../assets/style/mixins/mixin.scss';
@include button;
.header {
    width: 100%;
    position: absolute;
    top: 0;
    left: 0;
    &-wrapper {
        display: flex;
        align-items: center;
        justify-content: space-between;
        height: 90px;
    }
    &-logo {
        height: 40px;
        .logo {
            height: 100%;
        }
    }
    &-nav {
        display: flex;
        align-items: center;
        .list {
            display: flex;
            align-items: center;
            .item {
                margin: 0 1rem;
                color: white;
                font-weight: 400;
                .link {
                    display: flex;
                    &:hover {
                        color: $Yellow_Orange;
                    }
                    &.selected {
                        color: $Yellow_Orange;
                    }
                }
                .apply {
                    color: $Yellow_Orange;
                    border: 1.5px solid $Yellow_Orange;
                    margin-left: .5rem;
                    border-radius: 4px;
                    padding: .1rem .4rem;
                    text-transform: uppercase;
                    font-size: .8rem;
                }
            }
        }
        .button {
            background-color: $Yellow_Orange;
            &:hover {
                background-color: $Tulip_Tree-light-vibrant;
            }
        }
    }
}
</style>