<template>
    <div>
      <div class="myXhMyEvaluation"   color="#c62f2e">
        <van-tabs v-model="active">
          <van-tab title="全部">
            <div class="imgXhMyEvaluation">
<!--              <div>-->
<!--                <img src="https://assets-m.xinhuashudian.com/assets/files/comment-empty.9577180f12b0d799.png" alt="">-->
<!--                <p>暂无评价</p>-->
<!--              </div>-->
              <div class="evalutionimg">
                <img src="https://assets-m.xinhuashudian.com/assets/files/iconEmpty.b8f577481881acc5.png"/>
                <div class="numbermyevalution">
                  <p>1361****3235</p>
                  <van-rate
                    v-model="value"
                    :size="15"
                    color="#f44"
                    void-icon="star"
                    void-color="#eee"
                  />
                </div>
                <span>2019-06-24</span>
              </div>
            </div>
          </van-tab>
          <van-tab title="带图（0）">
            <div class="imgXhMyEvaluation">
<!--              <div>-->
<!--                <img src="https://assets-m.xinhuashudian.com/assets/files/comment-empty.9577180f12b0d799.png" alt="">-->
<!--                <p>暂无评价</p>-->
<!--              </div>-->
              <div class="evalutionimg">
                <img src="https://assets-m.xinhuashudian.com/assets/files/iconEmpty.b8f577481881acc5.png"/>
                <div class="numbermyevalution">
                  <p>1361****3235</p>
                  <van-rate
                    v-model="value"
                    :size="15"
                    color="#f44"
                    void-icon="star"
                    void-color="#eee"
                  />
                </div>
                <span>2019-06-24</span>
              </div>
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
            active:"",
            value: 5
          }
      }
    }
</script>

<style scoped>
  @import "../../assets/css/XhMyEvaluation.css";

</style>
