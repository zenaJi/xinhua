<template>
    <div>
      <div class="myXhMyEvaluation"   color="#c62f2e">
        <van-tabs v-model="active">
          <van-tab title="全部">
            <div class="imgXhMyEvaluation">
              <img src="https://assets-m.xinhuashudian.com/assets/files/comment-empty.9577180f12b0d799.png" alt="">
              <p>暂无评价</p>
            </div>
          </van-tab>
          <van-tab title="带图（0）">
            <div class="imgXhMyEvaluation">
              <img src="https://assets-m.xinhuashudian.com/assets/files/comment-empty.9577180f12b0d799.png" alt="">
              <p>暂无评价</p>
            </div>
          </van-tab>
          <van-tab title="追评（0）">
            <div class="imgXhMyEvaluation">
              <img src="https://assets-m.xinhuashudian.com/assets/files/comment-empty.9577180f12b0d799.png" alt="">
              <p>暂无评价</p>
            </div>
          </van-tab>
        </van-tabs>
      </div>
    </div>
</template>

<script>
    export default {
        name: "myXhMyEvaluationinner",
      data(){
          return{
            active:""
        }
      }
    }
</script>

<style scoped>
  @import "../../assets/css/XhMyEvaluation.css";

</style>
