<template>
        <div id="tabBar">
            <ul>
                <router-link 
                v-for="(item,index) in navs"
                :key="index"
                :to="item.path"
                tag="li"
                >
                <i>1</i>
                <span>{{item.text}}</span>
                </router-link>
            </ul>
        </div>
    </template>
    
    <script>
    export default {
        name:"TabBar",
        data(){
            return {
                navs:[
                    {
                        icon:"&#xe717;",
                        text:"电影",
                        path:"/details"
                    },
                    {
                        icon:"&#xe61d;",
                        text:"影院",
                        path:"/listening"
                    },
                    {
                        icon:"&#xe605;",
                        text:"我的",
                        path:"/ranking"
                    }
                ]
            }
        }
    }
    </script>
    
    <style>
        #tabBar{
            width: 100%;
            height: 1rem;
            position: fixed;
            left: 0;
            bottom:0;
            background: #fff;
            border-top:1px solid #ccc;
        }
        
        #tabBar ul,#tabBar ul li{
            width: 100%;
            height: 100%;
        }
        #tabBar ul{
            display: flex;
        }
        #tabBar ul li{
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            font-size:.3rem;
            color:black
        }
        #tabBar ul li i{
            font-size:.4rem;
        }
    
        #tabBar ul .router-link-active{
            color:#c33;
        }
    </style>