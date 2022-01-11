<template>
    <div class="hero">
        <div class="hero-bg">
            <img class="image" src="../../assets/images/1-hero-image.png" alt="hero background">
        </div>
        <div class="container">
            <div class="hero-content">
                <h1>SEM Campaigns Made Simple With Avada</h1>
                <div class="text">
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                    <p>Dolorum quos iure nobis ex totam dicta?</p>
                </div>
                <div class="buttons">
                    <button class="button">Buy avada now</button>
                    <button class="button"> Contact us</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Hero'
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/partials/variables.scss';
@import '../../assets/style/mixins/mixin.scss';
@include button;
.hero {
    width: 100%;
    height: 850px;
    display: flex;
    align-items: center;
    &-bg {
        position: absolute;
        top: 0;
        left: 0;
        z-index: -1;
        height: inherit;
        .image {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }
    &-content {
        width: 50%;
        color: white;
        .text {
            margin: 2rem 0;
            font-size: 1.5rem;
            line-height: 2.4rem;
        }
        .button:first-of-type {
            background-color: $Yellow_Orange;
            margin-right: 1.5rem;
            &:hover {
                background-color: $Tulip_Tree-light-vibrant;
            }
        }
        .button:last-of-type {
            background-color: $Science_Blue;
            &:hover {
                opacity: .9;
            }
        }
    }
}

</style>