<template>
  <div class="calendar">
    <div class="hello">{{msg}}</div>
      <section class="section-datetime">
          <div id="datetime" data-id="birthday">选择日期</div>
          <input type="hidden" id="birthday" name="birthday"  value="" ref="birthday" >
      </section>
    <button @click="test">测试</button>
  </div>
</template>

<script>
/* eslint-disable */ 

import lCalendar from '../libs/js/lCalendar.js'
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to js-lunar-calendar'
    }
  },
  //页面挂载时初始化日期插件
  mounted(){
    var calendar1 = new lCalendar().init('#datetime');
    new lCalendar().init('#dete');
  },
  methods:{
    test(){
      let glresult = this.$refs.birthday.value
      // deresult=result.substring(1, 2)
      // let cg=sloarToLunar(2015,10,20)
      console.log(glresult.substring(2, 12))
      let nlresult = $("#datetime").text().substring(3, 13)
      console.log(nlresult)
      let year = nlresult.substring(0,4)
      let mounth = nlresult.substring(5,7)
      let day = nlresult.substring(7)
      
      // console.log(day)
      //农历月份转数字
      var mmArr=new Array(['正月','二月','三月','四月','五月','六月','七月','八月','九月','十月','十一','十二'])
      for(var j = 0,len = mmArr.length; j < len; j++){
          if(mounth=='正月'){
            mounth='01'
          }
          if(mounth=='二月'){
            mounth='02'
          }
          if(mounth=='三月'){
            mounth='03'
          }
          if(mounth=='四月'){
            mounth='04'
          }
          if(mounth=='五月'){
            mounth='05'
          }
          if(mounth=='六月'){
            mounth='06'
          }
          if(mounth=='七月'){
            mounth='07'
          }
          if(mounth=='八月'){
            mounth='08'
          }
          if(mounth=='九月'){
            mounth='09'
          }
          if(mounth=='十月'){
            mounth='10'
          }
          if(mounth=='十一'){
            mounth='11'
          }
          if(mounth=='十二'){
            mounth='12'
          }
  
      }
      //农历日期转数字
      var ddArr=['初一','初二','初三','初四','初五','初六','初七','初八','初九','初十','十一','十二','十三','十四','十五','十六','十七','十八','十九','二十','廿一','廿二','廿三','廿四','廿五','廿六','廿七','廿八','廿九','三十','三十一'];
      for(var j = 0,len = ddArr.length; j < len; j++){
          if(day=='初一'|day=='初一 '|day=='月初一'){
            day='01'
          }
          if(day=='初二'|day=='初二 '|day=='月初二'){
            day='02'
          }
          if(day=='初三'|day=='初三 '|day=='月初三'){
            day='03'
          }
          if(day=='初四'|day=='初四 '|day=='月初四'){
            day='04'
          }
          if(day=='初五'|day=='初五 '|day=='月初五'){
            day='05'
          }
          if(day=='初六'|day=='初六 '|day=='月初六'){
            day='06'
          }
          if(day=='初七'|day=='初七 '|day=='月初七'){
            day='07'
          }
          if(day=='初八'|day=='初八 '|day=='月初八'){
            day='08'
          }
          if(day=='初九'|day=='初九 '|day=='月初九'){
            day='09'
          }
          if(day=='初十'|day=='初十 '|day=='月初十'){
            day='10'
          }
          if(day=='十一'|day=='十一 '|day=='月十一'){
            day='11'
          }
          if(day=='十二'|day=='十二 '|day=='月十二'){
            day='12'
          }
          if(day=='十三'|day=='十三 '|day=='月十三'){
            day='13'
          }
          if(day=='十四'|day=='十四 '|day=='月十四'){
            day='14'
          }
          if(day=='十五'|day=='十五 '|day=='月十五'){
            day='15'
          }
          if(day=='十六'|day=='十六 '|day=='月十六'){
            day='16'
          }
          if(day=='十七'|day=='十七 '|day=='月十七'){
            day='17'
          }
          if(day=='十八'|day=='十八 '|day=='月十八'){
            day='18'
          }
          if(day=='十九'|day=='十九 '|day=='月十九'){
            day='19'
          }
          if(day=='二十'|day=='二十 '|day=='月二十'){
            day='20'
          }
          if(day=='廿一'|day=='廿一 '|day=='月廿一'){
            day='21'
          }
          if(day=='廿二'|day=='廿二 '|day=='月廿二'){
            day='22'
          }
          if(day=='廿三'|day=='廿三 '|day=='月廿三'){
            day='23'
          }
          if(day=='廿四'|day=='廿四 '|day=='月廿四'){
            day='24'
          }
          if(day=='廿五'|day=='廿五 '|day=='月廿五'){
            day='25'
          }
          if(day=='廿六'|day=='廿六 '|day=='月廿六'){
            day='26'
          }
          if(day=='廿七'|day=='廿七 '|day=='月廿七'){
            day='27'
          }
          if(day=='廿八'|day=='廿八 '|day=='月廿八'){
            day='28'
          }
          if(day=='廿九'|day=='廿九 '|day=='月廿九'){
            day='29'
          }
          if(day=='三十'|day=='三十 '|day=='月三十'){
            day='30'
          }
          if(day=='三十一'|day=='三十一 '|day=='月三十一'){
            day='31'
          }
      }

      nlresult = year+'-'+mounth+'-'+day
      console.log(nlresult)
   }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello{
  color: #ff52ce;
}
.calendar{
  text-align: center;
  margin: 0 auto;
}
.calendarmain{
  margin-top: 50px
}
button {
  width: 200px;
  height: 50px;
  background: linear-gradient(#2d8d78, #52ebff);
  font-size: 20px;
  color: #fff;
  margin: 0.7rem auto;
  border: none;
  border-radius: 50px;
  display: block;
  box-shadow: 0 2px 4px rgba(255, 82, 206, 0.4);
}
</style>
