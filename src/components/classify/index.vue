<template>
        <div id = "classify">
            <div class = "classify-main">
                <router-link
                v-for = "(item,index) in list"
                :key = "index"
                tag = "div"
                :to="item.path"
                >    
                    <img :src="item.img" alt=""/>
                    <span>{{item.title}}</span>      
                </router-link>
            </div>
            <img src="../../../public/img/adv.png" alt="" class = "adv">
           
        </div>
        </template>
        <script>
            export default{
                name:"recoClassify",
                data(){
                    return{
                        list:[
                            {
                                img:"./img/1.png",
                                title:"排行榜",
                                path:"/ting/reman",
                            },
                            {
                                img:"./img/2.png",
                                title:"听单",
                                path:"/ting/reman",
                            },
                            {
                                img:"./img/3.png",
                                title:"摇滚",
                                path:"./ting",
                            },
                            {
                                img:"./img/4.png",
                                title:"民谣",
                                path:"./ting",
                            },
                            {
                                img:"./img/more.png",
                                title:"全部分类",
                                path:"./ting",
                            }
                        ]
                    }
                }
            }
        </script>    
    <style>
        #classify{
            width:100%;
            padding-top: .3rem
        }
    .classify-main{
        width:3.08rem;
        height:.54rem;
        position:relative;
        margin:auto;
        display: flex;
        align-items: center;
        justify-content: space-around;
      
    }
    .classify-main>div{
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
    .classify-main>div>img{
        width:.34rem;
        height: .34rem;
        border-radius: .34rem;
    }
    .adv{
        margin-top: .18rem;
        width:100%;
        height: .812rem;;
        margin-bottom: 8px;
    }      
    </style>