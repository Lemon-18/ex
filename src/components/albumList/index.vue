<template>
        <div id = "albums">
            <div class = "albums-content center">
                <div class = "title">
                        <span class = "classify-title">最新专辑</span>
                        <a href = "#" class = "more">更多<span>></span></a>
                    </div>
                    <ul class = "album-info">
                        <li>
                            <div>
                                <img src="../../../public/img/t3.jpg" alt="" class = "album-info-img">
                            </div>
                            <div class = "album-info-msg">
                                <p class = "msgtitle">习近平新时代中国特色社会主义思想学习纲要</p>
                                <p class = "msginfo">“不忘初心、牢记使命”主题教育重要学习材料</p>
                                <p class = "msgspan"><span><i class="iconfont">&#xe617;</i>&nbsp;&nbsp;学习出版社</span><span><i class="iconfont">&#xe606;</i>&nbsp;&nbsp;100</span><span><i class="iconfont">&#xe73a;</i>&nbsp;&nbsp;1000万</span></p>
                            </div>
                        </li>
                </ul>
            </div>
            
        </div>
    </template>
    <script>
    export default{
        name:"Album", 
    }
    </script>
    
    <style>
    .albums-content .title{
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
    .title .classify-title{
        font-size: .18rem;
        color: #333;
        font-weight: 700;
    }
    .title .more{
        font-size: .12rem;
    }
    .album-info li .album-info-img{
        width:.7rem;
        height: .7rem;
        border-radius: .05rem;
    }
    .album-info li{
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding-right: .1rem;
    }
    .album-info li .album-info-msg{
        height: .7rem;
        width:2.5rem;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-around
    }
    .album-info-msg>p{
        width:100%;
        overflow: hidden;
        white-space: nowrap;
        text-overflow: ellipsis;
    }
    .album-info-msg .msgtitle{
        font-size: .16rem;
        color :rgb(51, 51, 51);
        
    }
    .album-info-msg .msginfo,.album-info-msg .msgspan{
        font-size: .13rem;
        color: #999;
    }
    .album-info-msg .msgspan span{
        margin-right: .08rem;
    }
    .album-info-msg .msgspan span .iconfont{
        font-size: 0.12rem!important;
    }
    
    </style>