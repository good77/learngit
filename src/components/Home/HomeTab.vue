<template>
    <div id="HomeTab" class="HomeTab">
     <div class="HomeTab HomeCate">
         <div class="cate">
         <img  class="CateImage" src="../../assets/HomeCate/8.png">
         <div>特色</div>
         </div>
         <div class="cate">
         <img  class="CateImage" src="../../assets/HomeCate/1.png">
         <div>社交</div>
         </div>
         <div class="cate">
         <img  class="CateImage" src="../../assets/HomeCate/2.png">
         <div>情感</div>
         </div>
         <div class="cate">
         <img  class="CateImage" src="../../assets/HomeCate/3.png">
         <div>生活</div>
         </div>
         <div class="cate">
         <img  class="CateImage" src="../../assets/HomeCate/4.png">
         <div>娱乐</div>
         </div>
         <div class="cate">
         <img  class="CateImage" src="../../assets/HomeCate/5.png">
         <div>游戏</div>
         </div>
         <div class="cate">
         <img  class="CateImage" src="../../assets/HomeCate/6.png">
         <div>职业</div>
         </div>
         <div class="cate">
         <img  class="CateImage" src="../../assets/HomeCate/7.png">
         <div>文化</div>
         </div>
         <div class="cate">
         <img  class="CateImage" src="../../assets/HomeCate/10.png">
         <div>同城便</div>
         </div>
         <div class="cate">
         <img  class="CateImage" src="../../assets/HomeCate/9.png">
         <div>其他</div>
         </div>
         <!--<div v-for="image in Cate.IamgeUrl" :key="image">-->
             <!--<img  class="CateImage"  v-bind:src="image">-->
         <!--</div>-->
         <!--<div v-for="name in Cate.name" :key = "name">{{name}}</div>-->
     </div>


    </div>
</template>

<script>
    export default {
        name: "HomeTab",
        data(){

            return{
               Url:'../assets/HomeCate/',
               Cate:[],
            }
        },
        mounted:function(){
            this.$nextTick(function () {
                this.HomeTabView()
            })
        },
        methods:{
          HomeTabView:function () {
              var _this = this
           this.$axios.get('/index/all_cate')
               .then(function (response) {
                   var CateRes = response.data.data
                   var Catename = []
                   var CateImageUrl = []
                   for(var i in CateRes){
                       Catename[i] = CateRes[i].name
                       CateImageUrl[i] = _this.Url+CateRes[i].id+'.png'
                   }
                   _this.Cate.name = Catename
                   _this.Cate.ImageUrl =  CateImageUrl
                   console.log(_this.Cate)
                   console.log(response.data.data)
               })
               .catch(function (error) {
                   console.log(error)
               });
       }
        }
    }
</script>

<style scoped>
.HomeTab{
    width: 7.50rem;
    height: 3.50rem;
    display: flex;
    align-content: space-around;
    flex-wrap: wrap;
    font-size: .25rem;
}
.HomeTab.HomeCate{

}
.CateImage{
    width: .75rem;
    height: .80rem;
}
.cate{
    width:1.50rem;
    height: 1.20rem;
 }
</style>