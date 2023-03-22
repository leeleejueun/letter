<template>
    <dl>
        <div><dt>이름</dt><dd>{{data.name}}</dd></div>
        <div><dt>메일</dt><dd>{{data.email}}</dd></div>
        <div><dt>내용</dt><dd>{{data.content}}</dd></div>                
    </dl>
    {{d}}
    <router-link :to="{name:'about',query:data}">저장하기</router-link>

</template>
<script>
import {mapState} from 'vue';
export default {
    inject:['d'],
    name:'LetterView',
    props:{
        data:Object
    },

    computed:{
        
        ...mapState
    },
    updated(){
        this.d = 5000;
        console.log(this.data)
    }

}
</script>
<style lang="scss">
    dl{ background: #eee; padding:40px;
        div{border-bottom: 1px solid #000; padding:10px; display: flex;}
        div:last-child{min-height:200px;}
    }
</style>