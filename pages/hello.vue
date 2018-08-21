<template>
    <div>
      <p @click="get">{{aaa}}</p>
    </div>
</template>
<script>
    import axios from 'axios'

export default {

    data(){
        return{
            aaa:'111'
        }
    },
    mounted:function(){
        this.init();
    },
    methods:{
        init:function(){
            this.aaa = 222;
            
        axios.get('/api/api/getUserStatus').then(function(response){
            console.log(response);//请求正确时执行的代码
        }).catch(function (response){
            console.log(response);//发生错误时执行的代码
        });
        let a = 1;
        console.log(a)

        },
        get:function(){
            alert(this.aaa)
        }
    },

}
</script>

