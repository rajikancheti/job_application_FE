<template>
       <div class="job-card">
            <h3 class="ellipsis title">{{ job.position }}</h3>
            <p class="sub-title">{{ job.companyName }}</p>
            <span class="details">
                <p>{{ job.experience }}</p> | <p>{{ job.jobType }}</p> | <p :title="job.location" class="ellipsis">{{ job.location }}</p>
            </span>
       </div>
</template>

<script>
export default {
    props: {
        job: Object
    }
}
</script>

<style>
.job-card {
    width: 80%;
    padding: 15px;
    margin: auto;
    border-radius: 8px;
    z-index: 9997;
    background-color: #fff;
    white-space: normal;
    overflow: hidden;
    box-shadow: 0px 5px 5px 0px rgba(0,0,0,0.22), 0px 0px 6px 0px rgba(0,0,0,0.3);
}
.title {
    font-weight: 700;
    font-size: 16px;
    line-height: 22px;
    color: #121224;
    max-width: 100%;
    display: block;
}
.sub-title {
    font-weight: 600;
    font-size: 14px;
    line-height: 18px;
    color: #474d6a;
    max-width: 100%;
    display: inline-block;
}
.details {
    display: flex;
    margin-top: 20px;
}

.details p {
    padding: 0 10px;
    display: inline-block;
    font-weight: 500;
    font-size: 14px;
    line-height: 18px;
    color: #474d6a;
}
.ellipsis {
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
}
</style>