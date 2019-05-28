<template>
<div class="a">
<input type="text" v-model="text">
<button @click="aaa">提交</button>
<ul class="todo-list">
<li
v-for="(item,index) in list":key="index"
@click="qzk(index)"
>
{{item}}
</li>
</ul>


</div>
</template>

<script>
export default {
    name:'app',
    data() {
        return ({
            list: [
                '西瓜西瓜',
                '苹果苹果',
                '橘子橘子'
            ],
            text: ''
        })
    },
    methods:{
        aaa(){
            this.list.push(this.text),
            this.text = ''
        },
        qzk(index){
            this.list.splice(index,1)
        }
    }
}
</script>

<style>
.a{margin-left:30%;
width:500px;
height:300px;
border:2px solid brown;
    text-align:center;
}
.a input{
    border:2px solid green;
    background-color:red;
    
    width:400px;
    height:20px;
}
.a li{
    color:blue;
    list-style:none;
}
</style>
