<template>
  <div class="header">
    <div class="content-wrapper">
      <div class="avatar">
        <img width="64" height="64" :src="seller.avatar">
      </div>
      <div class="content">
        <div class="title">
          <span class="brand"></span>
          <span class="name">{{seller.name}}</span>
        </div>
        <div class="description">
          {{seller.description}}/{{seller.deliveryTime}}分钟送达
        </div>
        <div class="support">
          <span class="icon"></span>
          <span class="text">{{seller.supports[0].description}}</span>
        </div>
      </div>
    </div>
    <div class="bulletin-wrapper">

    </div>
  </div>
</template>
<script type="text/ecmascript-6">
export default{
  props:{
    seller:{
      type:Object
    }
  }
}


</script>
<style>
  .header{
  color: #fff;
  width: 100%;
  background: rgba(7, 17, 27, 0.5);
  }

  .content-wrapper{
  position: relative;
  padding: 24px 12px 18px 24px;
  font-size: 0;
  }
  .avatar{
  display: inline-block;
  vertical-align: top;
  }
  .avatar>img{
  border-radius: 2px;
  }
  .content{
  display: inline-block;
  margin-left: 16px;
  }
   .title{
      margin: 2px 0 8px 0;
   }
  .brand{
  display: inline-block;
  vertical-align: top;
  width: 30px ;
  height: 18px;
  background-size: 30px 18px;
  background-repeat: no-repeat;
  background-image: url("../../assets/img/brand@2x.png");
  }
   .name{
   margin-left: 6px;
    font-size: 16px;
    line-height: 18px;
    font-weight: bold;
   }
     .description{
     margin-bottom: 10px;
     line-height: 12px;
     font-size: 12px;
     }
     .support>.icon{
  display: inline-block;
  vertical-align: top;
  width: 12px;
  height: 12px;
  margin-right: 4px;
  background-size: 12px 12px;
  background-repeat: no-repeat;
  background-image: url("../../assets/img/decrease_1@3x.png");
  }
  .text{
  line-height: 12px;
  font-size: 10px;
  }
</style>
