<template>
  <div>
    {{msg}}

    <p v-for="(book ,index) in books">{{index}} : {{book}}</p>


    <div style="background-color:#ffaa22;">

      <p v-if="show" v-on:click="onWhoAreYou">你是谁</p>


      <button v-on:click="onClickMe">点我</button>


    </div>

  </div>
</template>

<script>
  export default {
    name: 'HelloWorld',
    data() {
      return {
        msg: 'hello,world',

        books:['30天精通Java','LAMP网站环境搭建','JS从入门到放弃'],

        show:true,

      }
    },


    methods:{
      onWhoAreYou(){
        alert("我是张三");
      },

      onClickMe(){
        this.show = !this.show;
      }
    }
  }
</script>


<style scoped>

</style>
