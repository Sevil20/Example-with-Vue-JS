<template>
<div>
  <!--v-once biz her hansi datani funksiya uzerinde deyisirikse , isteyirikse bu deyismesin bundan istifade edirik -->
  <h1 v-once>{{ text }}</h1>

  <!--v-bind directive birbasa atributlara mudaxile edir ozune birlesdirir-->
  <a  v-bind:href=" link ">Vue.js</a>

  <!--v-html-->
  <p v-html="linkother"></p>

  <!--v-text html textlerini oxuya bilmir-->
  <!-- <h3 v-text="text1"></h3> -->
</div>
  <div>
    <!--funkisiyadan gelen text-->
    <h3>{{ test() }}</h3>

  </div>

   <div>

<button v-on:click="test"> CLICK1</button> <hr>
<button @click="test"> CLICK2</button>

   </div>
</template>


<script >
// import HelloWorld from './components/HelloWorld.vue'
export default{
  data(){
    return{
      text:"Salam Dunya",
      link:"https://vuejs.org/",
      linkother:`<a href="https://vue.js.org/">Vue.js</a>`,
      text1:"<h1>Sevil</h1>"
    }
  },
  methods :{
    test(){
      return this.text = "Salam Sevil",alert("salam")
    }
   
  }

}

</script>
<style scoped>

</style>
