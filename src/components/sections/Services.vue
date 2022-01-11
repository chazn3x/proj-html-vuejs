<template>
    <section>
        <div class="container">
            <div class="services">
                <div class="section-title">
                    <h2 class="title">See Our Top Notch Services</h2>
                    <p class="text">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.</p>
                </div>
                <div class="cards">
                    <div class="card" v-for="(card, index) in cards" :key="index">
                        <a class="top" href="#">
                            <div class="icon">
                                <i :class="card.icon"></i>
                            </div>
                            <div class="title">
                                <h3>{{card.title}}</h3>
                            </div>
                        </a>
                        <div class="text">
                            <p>Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et dapibus faucibus odio.</p>
                        </div>
                        <a href="#" class="link">
                            Let's work together
                            <div class="icon">
                                <i class="fas fa-chevron-right"></i>
                            </div>
                        </a> 
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Services',
    data() {
        return {
            cards: [
                {
                    title: 'Google SEO',
                    icon: 'fab fa-google'
                },
                {
                    title: 'Brand Strategy',
                    icon: 'fas fa-cog'
                },
                {
                    title: 'Local SEO',
                    icon: 'fas fa-building'
                },
                {
                    title: 'SEO Analysis',
                    icon: 'fas fa-chart-bar'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/partials/variables.scss';
@import '../../assets/style/mixins/mixin.scss';
@include sectionTitle;
section {
    background: $Deep_Cove url(../../assets/images/pattern_background.png);
    background-size: cover;
}
.services {
    padding: 100px 0 150px;
    .section-title {
        color: white;
    } 
    .cards {
        display: grid;
        grid-template-columns: repeat(4, 24%);
        justify-content: space-between;
        margin-top: 100px;
        .card {
            width: 100%;
            background-color: $Lucky_Point;
            text-align: center;
            padding: 3rem 1.5rem;
            .top {
                transition: color .2s;
                color: white;
                .icon {
                    color: $Yellow_Orange;
                    font-size: 2rem;
                    margin-bottom: 2rem;
                }
                &:hover {
                    color: $Yellow_Orange;
                }
            }
            .text {
                font-size: 1.2rem;
                line-height: 2rem;
                color: white;
                margin-top: 1rem;
            }
            .link {
                color: $Yellow_Orange;
                display: flex;
                justify-content: center;
                align-items: flex-end;
                margin-top: 1rem;
                .icon {
                    font-size: .8rem;
                    margin-left: .2rem;
                }
            }
        }
    }
}
</style>