<script >
import jobsList from './components/jobs-list.vue';
import navHeader from './components/nav-header.vue'
    export default {
        data(){
            return {
                jobsList: []
            }
        },
        components: { jobsList, navHeader },
        methods: {
            async fetchData() {
                const response = await fetch('https://job-application-cpia.onrender.com/api');
                return await response.json();
            }
        },
        mounted() {
            this.fetchData().then(res => {
                if(res){
                    this.jobsList = res.data;
                }
                
            })
        }
    }
</script>

<template>
    <div class="main-container">
        <navHeader />
        <jobsList :jobsList="this.jobsList" />
    </div>
</template>

<style >
    .main-container {
        display: flex;
        flex-direction: column;
    }
</style>
