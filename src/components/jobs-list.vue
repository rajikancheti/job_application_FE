<template>
    <div class="sub-container">
    <section v-for="job in jobsList" :key="job.requisitionId" >
        <jobItem :job="job" />
    </section>
    </div>
</template>

<script>
import jobItem from './job-item.vue'
export default {
    components: {jobItem},
    props: {
        jobsList: Array
    }
}
</script>
<style>
.sub-container{
    padding: 15px;
}
section {
    margin-bottom: 20px;
}
</style>