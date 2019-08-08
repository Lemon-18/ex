<template>
    <div id = "tabBar">
        <ul class = "tab-container">
            <router-link
                v-for = "(item,index) in navList"
                :key = "index"
                :to = "item.path"
                tag = "li"
            >
                <a href = "#">{{item.text}}</a>
            </router-link>
        </ul>
    </div>
</template>
    
    <script>
    export default{
        name:"TabBar",
        data(){
            return{
                navList:[
                    {
                        path:"./home",
                        text:"推荐"
                    },
                    {
                        path:"./yousheng",
                        text:"有声书"
                    },
                    {
                        path:"./xiangsheng",
                        text:"相声"
                    },
                    {
                        path:"./ting",
                        text:"音乐"
                    },
                    {
                        path:"./xiangsheng",
                        text:"儿童"
                    },
                    {
                        path:"./yousheng",
                        text:"人文"
                    },
                    {
                        path:"./xiangsheng",
                        text:"情感"
                    },
                    {
                        path:"./yousheng",
                        text:"历史"
                    },
                    {
                        path:"./xiangsheng",
                        text:"科技"
                    },
                    {
                        path:"./yousheng",
                        text:"更多"
                    }],
                currentIndex :0
            }
        },
        methods:{
            clickHandler(index){
                this.currentIndex = index
            }  
        }
    }
    </script>
    
    <style>
    #tabBar{
        height: .45rem;
        padding-top: .05rem;
        display: flex;
        align-items: center;
        width: 100%;
        cursor: pointer;
        border-bottom: .005rem solid #e8e8e8;
        overflow-x: scroll;
    }
    .tab-container{
        height: .395rem;
        white-space: nowrap;
        display: flex;
        align-items: center;
    }

    .tab-container>li{
        height: 100%;
    }
    .tab-container li a{
        padding: .07rem .125rem;
        font-size: .14rem;
        color: #72727b;
        height: 100%;
        text-decoration: none;
        display: flex;
        align-items: center;
    }
    #tabBar ul .router-link-active{
       border-bottom: .03rem solid red
    }

    </style>