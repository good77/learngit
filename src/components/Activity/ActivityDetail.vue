<template>
    <div class="ActivityDetail">
        <mt-header title="" class="DetailTop">
            <router-link to="/Activity" slot="left">
                <mt-button icon="back" @click="Back" style="font-size: .25rem;font-weight: normal">活动详情</mt-button>
            </router-link>
            <!--<mt-button icon="more" slot="right" @click="more"></mt-button>-->
        </mt-header>
        <div class="DetailTitle">
            标题标题
        </div>
        <img class="DetailPic" src="../../assets/ActDetail.png">
        <div class="DetailContent">
            内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容
            内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容
            内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容
        </div>
        <img class="DetailPic" src="../../assets/ActDetail.png">
        <div class="DetailContent">
            内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容
            内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容
            内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容
        </div>
        <img class="DetailPic" src="../../assets/ActDetail.png">
        <div class="DetailContent">
            内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容
            内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容
            内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容
        </div>
        <img class="DetailPic" src="../../assets/ActDetail.png">
        <div class="DetailContent">
            内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容
            内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容
            内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容
        </div>
        <img class="DetailPic" src="../../assets/ActDetail.png">
        <div class="DetailContent">
            内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容
            内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容
            内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容
        </div>
        <div @click="ToTop" class="BackToTop">
            <i class="iconfont icon-back_to_top"></i>
            <div style="font-size: .1rem;color: #7C7B7B">顶部</div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "ActivityDetail",
        data(){
            return{

            }
        },
        methods:{
            Back:function () {
                console.log("返回")
            },
            ToTop:function () {
                document.body.scrollTop = 0
                document.documentElement.scrollTop = 0
            }
        }
    }
</script>

<style scoped>
    .ActivityDetail{
        display: flex;
        flex-direction:column;
    }
.DetailTop{
    width: 100%;
    height: .6rem;
}
.DetailTitle{
    font-size: .42rem;
    color: #000000;
}
.DetailPic{
    width: 100%;
    height: 4rem;
    margin:.1rem 0rem .2rem 0rem
}
.DetailContent{
    font-size: .16rem;
    color: #000000;
}
.BackToTop{
    width: .4rem;
    height: .5rem;
    display: flex;
    flex-direction: column;
    align-self: flex-end;
}
</style>