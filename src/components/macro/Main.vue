<template>
    <main>
        <Hero/>
        <div class="sections">
            <Agency/>
            <Services/>
            <Work/>
            <Plans/>
        </div>
    </main>
</template>

<script>
import Hero from '../elements/Hero.vue'
import Agency from '../sections/Agency.vue'
import Services from '../sections/Services.vue'
import Work from '../sections/Work.vue'
import Plans from '../sections/Plans.vue'
export default {
    name: 'Main',
    components: {
        Hero,
        Agency,
        Services,
        Work,
        Plans
    }
}
</script>

<style lang="scss" scoped>

</style>