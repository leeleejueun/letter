<template>
    <div class="write">
        <form>
            <input type="text" placeholder="이름" v-model="name"/>
            <input type="text" placeholder="이름" v-model="email"/>
            <textarea v-model="content"/>
            <input type="submit" value="전송" @click="dataSend"/>
        </form>
    </div>
</template>

<script>
export default {
    name:'LetterWrite',
    data(){
        return{
            name:'asdasdasd',
            email:'',
            content:'',
        }
    },
    methods:{
        dataSend(e){
            e.preventDefault();
            this.$emit('send',{name:this.name, email:this.email, content:this.content});
        }
    }
}
</script>
<style lang="scss">
    *{box-sizing: border-box;}
    .write{
        width:100%;
        input,textarea{width:100%; padding:10px;}
        textarea{height:400px;}
        
    }

</style>