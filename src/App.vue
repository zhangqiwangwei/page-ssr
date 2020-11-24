<template>
    <div id="app">
        <div><img alt="" src="//images.shesaidyes.com/home/pc/01.jpg" style="width: 100%;max-width: 100%;min-height: 40vw"></div>
        <div>test</div>
        <button @click="edit">edit9998</button>
        <ul>
            <li v-for="(item,index,key) in list1" :key="key">{{item.name}}</li>
        </ul>

        <ul>
            <li v-for="(item,index,key) in list" :key="key">{{item[0]}}</li>
        </ul>

    </div>
</template>
<script type="text/ecmascript-6">
    export default {
        components: {
        },
        data(){
            return {
                list1: [{name: "1"},{name: "2"}, {name: "3"}, {name: "4"}],
                list: [[22],[2], [3], [9]]
            }
        },
        methods: {
            edit(){
                console.log(this.list1);
                console.log(this.list)
                this.list1[2]["name"]= 8;
                this.list[2]= [8];
            },
            add(){
                console.log(this.list1);
            }
        }
    }
</script>
<style>
    body{
        margin: auto;
    }
    li{
        list-style: none;
        padding: 0;
    }
</style>