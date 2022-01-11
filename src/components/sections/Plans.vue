<template>
    <section>
        <div class="container">
            <div class="plans">
                <div class="section-title">
                    <h2 class="title">Our Plans</h2>
                    <p class="text">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.</p>
                </div>
                <div class="cards">
                    <div class="card" v-for="(card, index) in cards" :key="index">
                        <div class="card-wrapper">
                            <div class="title-row">
                                <h3>{{card.title}}</h3>
                            </div>
                            <div class="price-row">
                                <div class="price">
                                    <div class="row">
                                        <div class="currency">$</div>
                                        <div class="number big">{{card.price}}</div>
                                    </div>
                                    <div class="col">
                                        <div class="number small">99</div>
                                        <div class="period">monthly</div>
                                    </div>
                                </div>
                            </div>
                            <div class="info-row">
                                <div class="line">{{card.projects}} Projects</div>
                                <div class="line">{{card.storage}} Storage</div>
                                <div class="line">Unlimited Users</div>
                            </div>
                            <div class="button-row">
                                <a class="button" :class="{'unselected' : !card.selected}" href="#">Start today</a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Plans',
    data() {
        return {
            cards: [
                {
                    title: 'Standard',
                    price: '19',
                    projects: '5',
                    storage: '5 GB'
                },
                {
                    title: 'Premium',
                    price: '29',
                    projects: '10',
                    storage: '15 GB'
                },
                {
                    title: 'Professional',
                    price: '39',
                    projects: '15',
                    storage: ' 30 GB',
                    selected: true
                },
                {
                    title: 'Extreme',
                    price: '59',
                    projects: 'Unlimited',
                    storage: 'Unlimited'
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
@include button;
section {
    background-image: url(../../assets/images/background1.jpg);
    background-size: cover;
    background-position: center;
}
.plans {
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
            background-color: $Alabaster;
            text-align: center;
            padding: 1rem;
            &-wrapper {
                background-color: #fff;
                border: 2px solid white;
                border-right: 2px solid $Concrete;
                .title-row {
                    padding: 1rem 0;
                    color: $Science_Blue;
                    border-bottom: 2px solid $Concrete;
                }
                .price-row {
                    padding: 1.5rem 0;
                    background-color: $Alabaster;
                    .price {
                        display: flex;
                        justify-content: center;
                        .row {
                            display: flex;
                            align-items: flex-start;
                        }
                        .col {
                            display: flex;
                            flex-direction: column;
                            justify-content: space-between;
                            align-items: flex-start;
                        }
                        .number {
                            color: $Science_Blue;
                            &.big {
                                font-size: 3.5rem;
                                line-height: 2.5rem;
                                font-weight: 700;
                            }
                            &.small {
                                font-weight: 700;
                            }
                        }
                        .currency {
                            font-weight: 700;
                            font-size: 1.3rem;
                        }
                        .period {
                            font-style: italic;
                            margin-left: .3rem;
                            color: $Regent_Gray;
                            font-weight: 600;
                            font-size: .7rem;
                        }
                    }
                }
                .info-row {
                    color: $Scorpion;
                    font-size: 1.1rem;
                    .line {
                        margin: 2rem 0;
                    }
                }
                .button-row {
                    padding: 1.5rem 0;
                    background-color: $Alabaster;
                    .button {
                        background-color: $Yellow_Orange;
                        &:hover {
                            background-color: $Tulip_Tree-light-vibrant;
                        }
                        &.unselected {
                            color: $Scorpion;
                            background-color: transparent;
                            border-color: white;
                            &:hover {
                                color: $Science_Blue;
                                border-color: $Science_Blue;
                            }
                        }
                    }
                }
            }
        }
    }
}
</style>