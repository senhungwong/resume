<template>
    <div>
        <h2>Work Experience</h2>
        <div class="center-flex" v-for="experience in experiences" :key="experience.from">
            <experience
                :place="experience.company"
                :link="experience.link"
                :location="experience.location"
                :position="experience.title"
                :from="experience.from"
                :to="experience.to"
                :more="experience.more">
            </experience>
        </div>
    </div>
</template>

<script>
import Experience from '../templates/Experience';

export default {
    props: {
        experiences: Array
    },
    components: {
        Experience
    }
}
</script>

<style>

</style>
