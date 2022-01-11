<template>
    <main>
        <Hero/>
        <div class="sections">
            <Agency/>
            <Services/>
            <Work/>
            <Plans/>
            <News/>
            <Clients/>
        </div>
    </main>
</template>

<script>
import Hero from '../elements/Hero.vue'
import Agency from '../sections/Agency.vue'
import Services from '../sections/Services.vue'
import Work from '../sections/Work.vue'
import Plans from '../sections/Plans.vue'
import News from '../sections/News.vue'
import Clients from '../sections/Feedback.vue'
export default {
    name: 'Main',
    components: {
        Hero,
        Agency,
        Services,
        Work,
        Plans,
        News,
        Clients
    }
}
</script>

<style lang="scss" scoped>

</style>