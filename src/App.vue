<template>

<div class="d-flex vh-100  flex-column container">
  <h1 class="markdown text-center my-5 text-3xl">
    MarkdownApp
  </h1>

<section class=" row h-100">

<div class="col-6 border p-0 h-100">
  <textarea style="resize:none" v-model="text" class="h-100 w-100" placeholder="Digite o seu markdown aqui"></textarea>
</div>
<div  v-html="marked" class="col-6 border h-100 ">

</div>
</section>

</div>

</template>

<script>
import {marked} from 'marked';

export default {
methods: {


  }
,

  data(){
    return {
      text: '',
      timeout:''

    }
  },
  computed:{
    marked(){
      return marked(this.text)
    }
  },
  

  name: 'App',
  components: {
    
  }
}
</script>

<style>

</style>
