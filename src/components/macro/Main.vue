<template>
    <main>
        <Hero/>
        <div class="sections">
            <Agency/>
            <Services/>
            <Work/>
        </div>
    </main>
</template>

<script>
import Hero from '../elements/Hero.vue'
import Agency from '../sections/Agency.vue'
import Services from '../sections/Services.vue'
import Work from '../sections/Work.vue'
export default {
    name: 'Main',
    components: {
        Hero,
        Agency,
        Services,
        Work
    }
}
</script>

<style lang="scss" scoped>

</style>