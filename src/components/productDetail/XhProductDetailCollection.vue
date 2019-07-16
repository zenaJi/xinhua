<template>
<!--  收藏-->
    <div>
      <div class="CollectionProductDetail">
        <div class="Collection-box" >
          <p>￥{{detailData.lowPrice}}</p>
          <span v-if="detailData.lowPrice!==detailData.originalPrice" class="line-through">
            ￥{{detailData.originalPrice}}
          </span>
          <span  v-if="detailData.lowPrice!==detailData.originalPrice" class="DiscountCollectionProductDetail">
             {{detailData.discount}}
          </span>
        </div>
        <div @click="showCount" class="heartProductDetail">
          <div>
            <van-icon name="like-o"  v-show="showing" class="bProductDetail"  />
            <p v-show="showing">收藏</p>
          </div>
          <div v-show="!showing"  >
            <van-icon name="like" v-if="!showing" color="#c62f2e" style="font-size: .5rem"/>
            <p>已收藏</p>
          </div>
        </div>
      </div>
      <div class="TitleProductDetail">
        <p> {{detailData.title}}</p>
        <span v-show="detailData.advertise">{{detailData.advertise}}</span>
      </div>
    </div>
</template>

<script>
    export default {
      name: "XhProductDetailCollection",
      props:["detailData"],
      data() {
        return {
          // show: false,
          showing:true,
        }
      },
      methods: {
        showCount(){
          this.showing = !this.showing;
          // console.log(this.showing);
        },
      }
    }
</script>

<style scoped>
  @import "../../assets/css/XhProductDetail.css";

</style>
