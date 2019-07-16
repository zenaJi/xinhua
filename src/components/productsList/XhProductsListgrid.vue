<template>
<!--  两页列表-->
    <div>
          <div>
            <div class="gridproductsListsmall" v-for="(i,index) in allProducts" :key="index" @click="$router.push({name:'XhProductDetail',params:{goodsId:i.id}})">
            <div class="pri_boxsonlyProductsList">
                <img :src="'http://api.hll666.xyz/api/xinhua/img?imgUrl='+urlEncode(i.mainImage)" alt="">
              </div>
              <div class="gridsmall_box">
                <p class="aaXhProductsList"  >{{i.name}}</p>
                 <span class="bbXhProductsList" >{{i.author}}</span>
                <p class="ccXhProductsList"  >￥{{(i.lowPrice/100).toFixed(2)}}</p>
              </div>
            </div>
          </div>
    </div>
</template>

<script>
    export default {
        name: "XhProductsListgrid",
      props:["allProducts"],
      methods:{
        urlEncode(str){
          if(str.indexOf("https:")==-1){
            str="https:"+str
            return encodeURI(str)
          }else{
            return encodeURI(str)
          }
          // return encodeURI(str)
        }
      }
    }
</script>

<style scoped>
  @import "../../assets/css/XhProductsList.css";

</style>
