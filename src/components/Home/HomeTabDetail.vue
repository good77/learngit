<template>
    <div class="HomeTabDetail">
        <topBar/>
        <div class="Menu">
            <div class="MenuTab">
             <div  v-for="(MenuTab,index) in MenuTabs" :class="index === TabNum ? 'activeTab' : 'Tab'"
                 v-on:click="tab(index)" >{{MenuTab}}</div>
            </div>
            <div class="MenuDetail">
                <div class="DetailSwiper">
                    <HomeSwiper/>
                </div>

            </div>
        </div>
    </div>
</template>

<script>
    import topBar from '../topBar'
    import HomeSwiper from './HomeSwiper'
    export default {
        name: "HomeTabDetail",
        components:{
            topBar,
            HomeSwiper
        } ,
        data(){
            return{
                MenuTabs: ["同城便","社交","情感","生活","娱乐"],
                TabNum: 1,
            }
        },
        methods:{
            tab(index){
                this.TabNum = index;
                console.log(this.TabNum)
            }
        },
    }
</script>

<style scoped>
.HomeTabDetail{
    width: 7.5rem;
    height: 100%;
}
.Menu{
    display: flex;
    flex-direction: row;
}
.MenuTab{
    display: flex;
    flex-direction: column;
    width: 1.5rem;
 }
.activeTab{
    color: #DD5519;
    font-size: 23px;
    height: .8rem;
    background: #ffff;
    line-height: .7rem;
}
.Tab{
    font-size: 23px;
    height: .8rem;
    background: #eee;
    line-height: .7rem;
 }
.swiper-container{
    width: 6rem;
    height: 4.00rem;
    font-size: .50rem;
}
</style>