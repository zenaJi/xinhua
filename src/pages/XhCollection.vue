<template>
    <div class="XhCollection-cs">
      <div class="header-cs">
        <span class="iconfont icon-fanhui" @click="$router.back()"></span>
        <span class="set-cs">我的收藏</span>
        <div class="XhMyOrder-header-one" @click="exitCs" >
        	 <span>
        	 清空
        	</span>
        </div>
      </div>
			
      <van-tabs v-model="active" class="collect-cs" type="card">
        <van-tab title="商品收藏" class="collect-product">
										<div class="XhCollection-Bigbox">
											<div class="XhCollection-Bigbox-one-two">
													  <img src="../../static/images/mine/xhimg/4471015-fm.jpg" />
													  <div class="XhCollection-Bigbox-one-two-span"><span>破冰行动</span></div>
													  <div class="XhCollection-Bigbox-one-two-span">
														  <span class="XhCollection-Bigbox-one-two-span-span1">￥68.40</span>
											              
													  </div>
										</div>
										</div>
          <!-- <img src="../../static/cs/收藏.png">
          <span>去添加点什么吧</span>
          <router-link to="/" > <button>随便逛逛</button></router-link> -->
        </van-tab>
				
        <van-tab title="图书管理" class="collect-product">
          <img src="../../static/cs/收藏.png">
          <span>暂无图书馆收藏</span>
        <router-link to="/"> <button>随便逛逛</button></router-link>
					</van-tab>
        <van-tab title="活动收藏" class="collect-product">
          <img src="../../static/cs/收藏.png">
          <span>暂无活动收藏</span>
          <router-link to="/"> <button>随便逛逛</button></router-link>
					</van-tab>
      </van-tabs>
    </div>
</template>

<script>
	import { Dialog } from 'vant';
	import { Toast } from 'vant';
    export default {
        name: "XhCollection",
      data() {
        return {
          active: 0
        }
        },
				methods:{
				    exitCs(){
				      Dialog.confirm({
				        title: '提示',
				        message: '确定要删除所以商品收藏?',
				        confirmButtonColor:"#c72f2e",
								
				      }).then(() => {
				        // on confirm
								this.$toast('删除成功');
				      }).catch(() => {
				        // on cancel
									
				      });
				    }
					
				},
				components: {
				  [Dialog.Component.name]: Dialog.Component
				},
			
    }
</script>

<style scoped>
	.XhMyOrder-header-one{
		float: right;
		width: 1rem;
		height: 1rem ;
		margin-right: .2rem;
	}
	.XhMyOrder-header-one span{
		font-size: 16px !important;
		line-height: .7rem;
	}
  .XhCollection-cs{
    background-color: #f7f7f7;
    height: 100%;
    width: 100%;
    text-align: center;
    padding: 0 0.3rem;
    font-size: 15px;
  }
  .XhCollection-cs .header-cs{
    font-size: 16px;
    height: 0.8rem;
    line-height: 0.8rem;
    /*background-color: red;*/
  }
  .XhCollection-cs .header-cs .icon-fanhui{
    float: left;
    color: red;
  }
  .XhCollection-cs .header-cs .set-cs{
    /*margin-right: 0.16rem;*/
  }
  .XhCollection-cs .header-cs span:last-child{
    float: right;
    font-size: 12px;
  }
  .XhCollection-cs .collect-cs{
    margin-top: 0.2rem;
  }
  .XhCollection-cs .collect-cs img{
    width: 2.4rem;
    height: 2.4rem;
  }
  .XhCollection-cs .collect-product{
    display: flex;
    flex-direction: column;
    height: 7rem;
    align-items: center;
    /* justify-content: center; */
  }
  .XhCollection-cs .collect-product span{
    color: #cccccc;
    font-size: 14px;
  }
  .XhCollection-cs .collect-product button{
    width: 3rem;
    height: 0.8rem;
    border: none;
    background-color: #c72f2e;
    margin-top: 0.5rem;
    color: white;
  }
.XhCollection-box-one-two{
	width: 100%;
	height: 2rem;
	border-bottom: 1px solid #cfcfcf;
}
.XhCollection-box-one-two img{
	width: 2rem;
	height: 1.8rem;
	float: left;
	margin-top: .1rem;
}
.XhCollection-box-one-two-span span{
	float: left;
	font-size: 16px;
	line-height: 1rem;
	margin-left: .2rem;
	}
	.XhCollection-box-one-two-span{
		width: 5rem;
		height: 1rem;
		float: right;
	}	
	.XhCollection-box-one-two-span-span1{
		color: red;
	}
	.XhCollection-box-one-two-span-span2{
		float: right !important;
		color: #999999;
		margin-right: .2rem;
	}
	.XhCollection-Bigbox{
		width: 100%;
		flex:1;
		overflow-y:auto;
		background: #f7f7f7;
	}
	.XhCollection-Bigbox-one-two{
		width: 100%;
		height: 2.5rem;
		background: white;
		margin-top: .3rem;
	}
.XhCollection-Bigbox-one-two img{
	width: 2rem;
	height: 1.8rem;
	float: left;
	margin-top: .1rem;
}
.XhCollection-Bigbox-one-two-span span{
	float: left;
	font-size: 16px;
	line-height: 1.25rem;
	margin-left: .2rem;
	}
.XhCollection-Bigbox-one-two-span{
	width: 5rem;
	height: 1.25rem;
	text-align: left;
}	
.XhCollection-Bigbox-one-two-span-span1{
	color: red !important;
	line-height: 1.25rem;
}

</style>
