<template>
    <div id="Activity" class="Activity">
        <div class="ActivityTitle">
            <div class="Title">活动专区</div>
        </div>
        <ActivitySwiper/>
        <ActivityNavbar/>
    </div>
</template>

<script>
    import ActivitySwiper from './ActivitySwiper'
    import ActivityNavbar from './ActivityNavbar'
    export default {
        name: "Activity",
        components:{
           ActivitySwiper,
           ActivityNavbar
        }
    }
</script>

<style scoped>
.Activity{
        display: flex;
        width: 7.50rem;
        flex-direction: column;
}
.ActivityTitle{
    width: 7.50rem;
    height: .90rem;
    background: darkorange;
    font-size: 0.40rem;
    color: #ffff;
    text-align: center;
}
.Title{
    margin-top: .15rem;
}
</style>