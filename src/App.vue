<template>
  <div id="app">
    <div id="nav">
      <router-link to="/Home"></router-link>
    </div>
    <router-view/>
  </div>
</template>

<style lang="less">
  @import "http://at.alicdn.com/t/font_792290_jmpwmk9dcbr.css";
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

blockquote,body,button,dd,dl,dt,fieldset,form,h1,h2,h3,h4,h5,h6,hr,input,legend,li,ol,p,pre,td,textarea,th,ul {margin:0;padding:0}  
h1,h2,h3,h4,h5,h6 {font-size:100%}  
address,cite,dfn,em,var {font-style:normal}  
code,kbd,pre,samp {font-family:courier new,courier,monospace}  
small {font-size:12px}  
ol,ul {list-style:none}  
a {text-decoration:none}  
a:hover {text-decoration:underline}  
sup {vertical-align:text-top}  
sub {vertical-align:text-bottom}  
legend {color:#000}  
fieldset,img {border:0}  
button,input,select,textarea {font-size:100%}  
table {border-collapse:collapse;border-spacing:0} 
/*#nav {*/
  /*padding: 30px;*/
  /*a {*/
    /*font-weight: bold;*/
    /*color: #2c3e50;*/
    /*&.router-link-exact-active {*/
      /*color: #42b983;*/
    /*}*/
  /*}*/
/*}*/
html {
  font-size: 13.333333333333334vw!important; /* 100vw / 750 * 100 */
}
</style>
