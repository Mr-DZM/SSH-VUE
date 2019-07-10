<template>
  <div class="container">
    <div class="ctrl">
        <span v-for="(item,index) in ['新闻','体育','游戏']"
        :key="index"
        @click='hanleClick(index)'
        :class="{active:current===index}"
        >
            {{item}}
        </span>
    </div>
     <div v-if="current === 0">
            <ul>
                <li>宋仲基离婚</li>
                <li>宋仲基离婚</li>
                <li>宋仲基离婚</li>
            </ul>
        </div>
        <div v-if="current === 1">
            <ul>
                <li>蔡徐坤打篮球</li>
                <li>蔡徐坤打篮球</li>
                <li>蔡徐坤打篮球</li>
            </ul>
        </div>
        <div  v-if="current === 2">
            <ul>
                <li>落地98k</li>
                <li>落地98k</li>
                <li>落地98k</li>
            </ul>
        </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      current:0,
    }
  },
  methods: {
    hanleClick(idnex){
      this.current=index
    }
  }
}
</script>

<style>
    .ctrl{
        margin-bottom:10px;
    }

    .ctrl span{
        cursor: pointer;
        margin:0 10px;
    }

    .active{
        color:red;
    }
</style>
