<template>
  <div class="home">
    
    <article>
      <h2>Write</h2>
      <LetterWriteVue @send="letterSend"/>
    </article>

    <article>
      <h2>Preview</h2>
      <LetterViewVue :data="WriteInfo"/>
    </article>
    
  </div>
</template>

<script>
import LetterViewVue from '../components/LetterView.vue'
import LetterWriteVue from '../components/LetterWrite.vue'
// @ is an alias to /src


export default {
  name: 'HomeView',
  components: {
    LetterViewVue, LetterWriteVue
  },
  data(){
    return{
      WriteInfo : ''
    }
  },
  methods:{
    letterSend(value){
      this.WriteInfo = value
    }
  }

}
</script>

<style lang="scss">
.home{
  display: flex; justify-content: space-between;
  width:80%; margin:100px auto; 
  article{width:48%;}
}
</style>
