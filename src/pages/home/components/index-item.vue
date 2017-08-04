<template>
    <div class="index-item" v-if="itemMetas.isHomeHeaderModel">

	<div class="index-warp">
		<ul class="index-main index-content">
			<li><a href="https://aflow.dingtalk.com/dingtalk/mobile/homepage.htm?corpid=dingf8bfabd87f8ad90f&showmenu=false&dd_share=false&swfrom=work_homepage#upcoming">待办事宜<span class="index-main-span">10</span></a></li>
			<li><a href="dingtalk://dingtalkclient/action/switchtab?index=2&name=work&scene=1&corpid=dingf8bfabd87f8ad90f&appid=-4">移动审批</a></li>
			<li><a href="dingtalk://dingtalkclient/action/switchtab?index=2&name=work&scene=1&corpid=dingf8bfabd87f8ad90f&appid=2">工作日志</a></li>
			<li><a href="dingtalk://dingtalkclient/action/switchtab?index=2&name=work&scene=1&corpid=dingf8bfabd87f8ad90f&appid=158">考勤打卡</a></li>
		</ul>
		<ul class="index-main1 index-content">
			<li><a href="javascript:;">我的应用</a></li>
			<li><a href="javascript:;">ERP系统集成</a></li>
			<li><a href="javascript:;">业务后台集成</a></li>
			<li class="index-main1-li"></li>
		</ul>
		<div class="index-main2 index-content">
			<ul class="index-main2-ul index-main2-ul1 index-content">
				<li><a href="https://attendance.dingtalk.com/attendance/mobile/mapAttendance.html?corpid=dingf8bfabd87f8ad90f&showmenu=true&dd_progress=true&dd_share=false">电话会议</a></li>
				<li><a href="javascript:;">视频会议</a></li>
				<li><a href="javascript:;">办公电话</a></li>
				<li><a href="javascript:;">钉盘</a></li>
				<li><a href="javascript:;">会议室预定</a></li>
				<li><a href="javascript:;">智能报表</a></li>
				<li><a href="javascript:;">公告</a></li>
				<li><a href="javascript:;">签到</a></li>
				<li><a href="javascript:;">文件柜</a></li>
				<li><a href="javascript:;">考勤</a></li>
				<li><a href="javascript:;">工作日志</a></li>
				<li><a href="javascript:;">移动审批</a></li>
				<li><a href="javascript:;">知识库</a></li>
				<li><a href="javascript:;">钉邮</a></li>
				<li><a href="javascript:;">企业红包</a></li>
			</ul>
			<ul class="index-main2-ul index-content">
				<li><a href="javascript:;">电话会议</a></li>
				<li><a href="javascript:;">视频会议</a></li>
				<li><a href="javascript:;">办公电话</a></li>
				<li><a href="javascript:;">钉盘</a></li>
				<li><a href="javascript:;">会议室预定</a></li>
				<li><a href="javascript:;">智能报表</a></li>
				<li><a href="javascript:;">公告</a></li>
				<li><a href="javascript:;">签到</a></li>
				<li><a href="javascript:;">文件柜</a></li>
				<li><a href="javascript:;">考勤</a></li>
				<li><a href="javascript:;">工作日志</a></li>
				<li><a href="javascript:;">移动审批</a></li>
				<li><a href="javascript:;">知识库</a></li>
				<li><a href="javascript:;">钉邮</a></li>
				<li><a href="javascript:;">企业红包</a></li>
			</ul>
			<ul class="index-main2-ul index-content">
				<li><a href="javascript:;">电话会议</a></li>
				<li><a href="javascript:;">视频会议</a></li>
				<li><a href="javascript:;">办公电话</a></li>
				<li><a href="javascript:;">钉盘</a></li>
				<li><a href="javascript:;">会议室预定</a></li>
				<li><a href="javascript:;">智能报表</a></li>
				<li><a href="javascript:;">公告</a></li>
				<li><a href="javascript:;">签到</a></li>
				<li><a href="javascript:;">文件柜</a></li>
				<li><a href="javascript:;">考勤</a></li>
				<li><a href="javascript:;">工作日志</a></li>
				<li><a href="javascript:;">移动审批</a></li>
				<li><a href="javascript:;">知识库</a></li>
				<li><a href="javascript:;">钉邮</a></li>
				<li><a href="javascript:;">企业红包</a></li>
			</ul>
		</div>
	</div>
    </div>
</template>

<script>
    import { openLink } from '../../../lib/util.js';
    var lock = true;
    export default{
        name: 'item',
        props: ['corpId','itemMetas'],
        data: function () {
            return {

            };
        },
        methods: {
            appLink: function (url) {
                // alert(url);
                if (lock){
                    lock = false;
                    openLink(url, function(){
                        lock = true;
                    });
                }
            }
        }


    }




</script>

<style>
    .index-item{
        position: relative;
        width: 100%;
        height: auto;
        margin-bottom: 17px;
        background-color: #fff;
    }
    .index-item-center{
        position: relative;
        height: 270px;
        background-color: #fff;
        overflow: hidden;
    }

    .index-warp{
    	width:100%;
    	height:auto;
    }
    .index-main1 .index-main1-li a{
        color:#1e82d2;
        border-bottom:2px solid #1e82d2;
    }
    .index-main1 .index-main1-li{
        position:absolute;
        left:0;
        bottom:0;
        border-bottom:2px solid #1e82d2;
        width:33.333333%;
        height:0;

    }
    .index-item-con{
        width: 100%;
        height: 80px;
        display: flex;
        padding-top: 11px;
        padding-bottom: 18px;
        flex-direction: row;
        justify-content: space-between;
        border-bottom-color: #eee;
        border-bottom-style: solid;
        border-bottom-width: 1px;
    }

    .item{
        flex: 1;
        margin-right: 1px;
    }

    .item-right-line{
        border-right-color: #eee;
        border-right-style: solid;
        border-right-width: 1px;
    }

    .item-number{
        font-size:24px;
        font-weight: 500;
        text-align: center;
    }
    .item-text{
        font-size: 13px;
        color: #999;
        margin-top: 4px;
        padding-bottom: 4px;
        text-align: center;
    }

/*==============index*/
.index-warp{
	width:100%;
	height:auto;
}
.index-main{
	width:90%;
	height:auto;
	padding:0.8rem 5%;

}
.index-main li{
	width:25%;
	height:3rem;
	float:left;
	background:url(../images/right_bg_05.png) no-repeat right center;
	background-size:0.1rem 2rem;
}
.index-main li a{
	display:block;
	width:100%;
	height:0.8rem;
	text-align:center;
	font-size:0.9rem;
    font-family: "黑体";
    line-height:0.9rem;
    color: #333333;
    padding-top:2.2rem;
    position:relative;
}
.index-main-span{
	display:block;
	width:1.1rem;
	height:1.1rem;
	border-radius:50%;
	-webkit-border-radius:50%;
	-moz-border-radius:50%;
	-ms-border-radius:50%;
	-o-border-radius:50%;
	background:#f13b3b;
	text-align:center;
	line-height:1.2rem;
	color:#fff;
	position:absolute;
	right:14%;
	top:0.1rem;
	font-size:0.3rem;
}
@media screen and (max-width: 400px){
	.index-main-span{
		right:10%;
	}

}
@media screen and (max-width: 320px){
	.index-main-span{
		right:6%;
	}

}
.index-main li:nth-of-type(1) a{
	background:url(../images/daiban.png) no-repeat center 0.3rem;
	background-size:1.6rem auto;
}
.index-main li:nth-of-type(2) a{
	background:url(../images/yidong.png) no-repeat center 0.3rem;
	background-size:1.5rem auto;
}
.index-main li:nth-of-type(3) a{
	background:url(../images/gongzuo.png) no-repeat center 0.3rem;
	background-size:1.5rem auto;
}
.index-main li:nth-of-type(4){
	background:#fff;
}
.index-main li:nth-of-type(4) a{
	background:url(../images/kaoqin.png) no-repeat center 0.3rem;
	background-size:1.2rem auto;
}
.index-main1{
	clear:both;
	width:100%;
	height:2.5rem;
	border-top:0.4rem solid #f2f4f5;
	position:relative;
}
.index-main1 li{
	width:33.333333%;
	height:2.5rem;
	float:left;
}
.index-main1 li a{
	display:block;
	width:100%;
	height:2.5rem;
	line-height:2.5rem;
	text-align:center;
	font-size:0.9rem;
    font-family: "黑体";
    color: #333333;
    border-bottom:1px solid #dedfe5;
    box-sizing:border-box;
    -webkit-box-sizing:border-box;
    -moz-box-sizing:border-box;
    -ms-box-sizing:border-box;
    -o-box-sizing:border-box;
}
.index-main1 .index-main1-li a{
	color:#1e82d2;
	border-bottom:2px solid #1e82d2;
}
.index-main1 .index-main1-li{
	position:absolute;
	left:0;
	bottom:0;
	border-bottom:2px solid #1e82d2;
	width:33.333333%;
	height:0;

}
.index-main2{
	width:90%;
	height:auto;
	padding:1rem 5%;
}
.index-main2-ul{
	width:100%;
	height:auto;
	display:none;

}
.index-main2-ul1{
	display:block;
}
.index-main2-ul li{
	width:25%;
	height:auto;
	float:left;
}
.index-main2-ul li a{
	display:block;
	width:100%;
	height:0.8rem;
	padding-top:3.2rem;
	font-size:0.9rem;
    font-family: "黑体";
    color:#333;
    line-height:0.8rem;
    text-align:center;
    padding-bottom:0.5rem;
}

@media screen and (max-width: 320px){
	.index-main2-ul li a{
		padding-bottom:0rem;
	}

}
.index-main2-ul li:nth-of-type(1) a{
	background:url(../images/dianhua.png) no-repeat center 0.8rem;
	background-size:2rem auto;
}
.index-main2-ul li:nth-of-type(2) a{
	background:url(../images/ship.png) no-repeat center 0.8rem;
	background-size:1.9rem auto;
}
.index-main2-ul li:nth-of-type(3) a{
	background:url(../images/bang.png) no-repeat center 0.8rem;
	background-size:1.9rem auto;
}
.index-main2-ul li:nth-of-type(4) a{
	background:url(../images/dingpan.png) no-repeat center 0.8rem;
	background-size:1.9rem auto;
}
.index-main2-ul li:nth-of-type(5) a{
	background:url(../images/hyyd.png) no-repeat center 0.8rem;
	background-size:1.8rem auto;
}
.index-main2-ul li:nth-of-type(6) a{
	background:url(../images/znbb.png) no-repeat center 0.8rem;
	background-size:1.6rem auto;
}
.index-main2-ul li:nth-of-type(7) a{
	background:url(../images/gg.png) no-repeat center 0.9rem;
	background-size:1.6rem auto;
}
.index-main2-ul li:nth-of-type(8) a{
	background:url(../images/qd.png) no-repeat center 0.8rem;
	background-size:1.6rem auto;
}
.index-main2-ul li:nth-of-type(9) a{
	background:url(../images/wjg.png) no-repeat center 1rem;
	background-size:1.7rem auto;
}
.index-main2-ul li:nth-of-type(10) a{
	background:url(../images/kq.png) no-repeat center 0.8rem;
	background-size:1.5rem auto;
}
.index-main2-ul li:nth-of-type(11) a{
	background:url(../images/rz.png) no-repeat center 0.8rem;
	background-size:1.6rem auto;
}
.index-main2-ul li:nth-of-type(12) a{
	background:url(../images/sp.png) no-repeat center 0.8rem;
	background-size:1.6rem auto;
}
.index-main2-ul li:nth-of-type(13) a{
	background:url(../images/zsk.png) no-repeat center 0.8rem;
	background-size:1.6rem auto;
}
.index-main2-ul li:nth-of-type(14) a{
	background:url(../images/dy.png) no-repeat center 0.8rem;
	background-size:1.9rem auto;
}
.index-main2-ul li:nth-of-type(15) a{
	background:url(../images/hb.png) no-repeat center 0.8rem;
	background-size:1.6rem auto;
}
/*==============index*/
/*==============tupian  chajian*/
.addWrap{
	position:relative;
	width:100%;
	background:#fff;
	margin:0;
	padding:0;
}
.addWrap .swipe{
	overflow: hidden;
	visibility: hidden;
	position:relative;
}
.addWrap .swipe-wrap{
	overflow:hidden;
	position:relative;
}
.addWrap .swipe-wrap > div {
	float: left;
	width: 100%;
	position:relative;
}
.addWrap .swipe-wrap > div a,.addWrap .swipe-wrap > div a img{
	display:block;
	width:100%;
	height:auto;
	margin:0 auto;
}
#position{
	position:absolute;
	height:26px;
	bottom:0;
	right:3px;
	margin:0;
	width:100%;
	text-align:right;
}
#position li{
	width:10px;
	height:10px;
	margin:10px 2px 0;
	display:inline-block;
	-webkit-border-radius:5px;
	border-radius:5px;
	background-color:#aaaaaa;
}
#position li.cur{
	background-color:#fff;
}
.img-responsive {
	display: block;
	max-width:100%;
	height: auto;
}
/*==============tupian  chajian*/

/* CSS Document */

html, body, ul, li, ol, dl, dd, dt, p, h1, h2, h3, h4, h5, h6, form, fieldset, legend, img,input{
	margin:0;padding:0;
}
body{
	font:12px/19px Arial, Helvetica, sans-serif,"宋体";
}
fieldset,img{
	border:0;
}
ul,ol{
	list-style:none;}
img {
	border:none;
	display:block;
}

a {
	text-decoration:none;
}

.index-content:before {
	content: ".";
	display: block;
	height: 0px;
	clear: both;
	visibility: hidden;
}
.index-content{
	display:inline-block;
	*display:inline;
	*zoom:1;
}
p{
	word-break:break-all;
}

input[type="button"], input[type="submit"], input[type="reset"] {

}

textarea {  -webkit-appearance: none;}
.button{ border-radius: 0; }

input:focus,input:visited,input:hover{

    outline:none;
}
a,.tape3-top2,.tape3-top3 div{
	tap-highlight-color:rgba(0,0,0,0);

}
input,input:focus,textarea:focus ,,a:focus{
    outline: none;

}
input::-ms-clear {
    display: none;
}
textarea {
    resize: none;
}
a,button,input,textarea{

}

html {
　-webkit-text-size-adjust: 100%;

}

</style>
