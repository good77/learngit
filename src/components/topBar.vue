<template>
    <div class="TopBar">
      <div class="City">
          <div class="CityName">武汉</div>
          <i class="iconfont icon-jiantou" style="color: white"></i>
      </div>
      <div class="Search">
           <i class="iconfont icon-search" style="margin-top: 0.1rem;"></i>
          <input class="SearchInput" placeholder="文献翻译">
      </div>
    </div>
</template>

<script>
    export default {
        name: "topBar"
    }
</script>

<style scoped>
  .TopBar{
      width: 7.50rem;
      height: .90rem;
      display: flex;
      justify-content: space-evenly;
      background: darkorange;
  }
  .City{
      flex-direction: row;
      display: flex;
      align-items: baseline;
  }
  .CityName{
      color: white;
      margin-top: .20rem;
      font-size: .35rem;
}
  .Search{
      width: 6.15rem;
      height: .50rem;
      background: white;
      margin-top: .18rem;
      border-radius: .15rem;
      display: flex;
      justify-content: space-evenly;
  }
  .SearchInput{
      width: 5.00rem;
      height: .45rem;
      font-size: .28rem;
      border: 0;
      outline: none;
  }
  .iconfont{
      font-size: .30rem;
  }
</style>