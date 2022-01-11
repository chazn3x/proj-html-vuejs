<template>
    <section>
        <div class="cta">
            <div class="section-title">
                <h2 class="title">Start Your Free Consultation</h2>
                <p class="text">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.</p>
            </div>
            <a href="#" class="button">Contact us now</a>
        </div>
    </section>
</template>

<script>
export default {
    name: 'CallToAction'
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/partials/variables.scss';
@import '../../assets/style/mixins/mixin.scss';
@include sectionTitle;
@include button;
section {
    background: url(../../assets/images/CTA-seo-1.jpg);
    background-size: cover;
    background-position: center;
}
.cta {
    padding: 100px 0;
    background-color: rgba(0,0,0,0.6);
    text-align: center;
    .section-title {
        color: white;
    }
    .button {
        margin-top: 2rem;
        background-color: $Yellow_Orange;
        &:hover {
            background-color: $Tulip_Tree-light-vibrant;
        }
    }
}
</style>