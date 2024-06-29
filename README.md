<!DOCTYPE html>
<html>
  <head>
    <title>目录</title>
    <meta charset="utf-8" />
    <style type="text/css">
      /* 公用样式 */
      html,body{
	    width:100%;
      	height:100%;
      	margin:0px;
		background-image: url("img/1.0.jpg");
		background-color: #000000;
		background-repeat:no-repeat;
		background-size:cover;
      }
      ul{
	    list-style-type:none;
      	margin:0px auto;
      	padding:0px;
      }
      
      /* 导航菜单 */
      .menu{
      	background-color:#0099ff ;
		display: flex;
      	color:#ffffff;
      	width:100%;
		justify-content: center;
      }
      .menu ul{
	    width:100%;
      	background-color:#0099ff ;
      	display:flex;
      	justify-content:center;
      }
      .menu ul li{
	    width:200px;
      	line-height:50px;
      	text-align:center;
      }
		a{
			color:#ffffff;
            text-decoration:none;
            margin-left:50px;
			}
            a:hover{
            color:#FF0000;
            text-decoration:underline;
            }
            a:hover img{
              opacity:0.5;
			}
      /* 图片列表 */
      .image_list{
      	margin:50px auto 0px auto;
	    width:80%;
      	height:70%;
		
		opacity:1;
      }
      .image_list ul{
	    width:115%;
      	height:100%;
		
      	display:flex;
      	justify-content:space-around;
      }
      .image_list ul li{
      	width:100%;
      	height:100%;
      	border-radius:25px;
      	
      	background-position:center;
      	background-repeat:no-repeat;
      	background-size:auto 100%;
      	
      	opacity:0.7;
      }
      .image_list ul li:hover{
        opacity:1;
      }
      .image_list ul li:nth-of-type(1){
	    background-image:url("img/雷锋塔.webp");
      }
      .image_list ul li:nth-of-type(3){
	    background-image:url("img/苏堤.webp");
      }
      
      .image_list ul li:nth-of-type(5){
        background-image:url("img/断桥.webp");
      }
      
      .image_list ul li:nth-of-type(7){
        background-image:url("img/龙井山.webp");
      }


  
  /* 雨滴样式 */  
  .raindrop {  
    position: absolute;  
    bottom: 100%;  
    width: 2px;  
    height: 100px;  
    background: linear-gradient(rgba(255, 255, 255, 0), rgba(255, 255, 255, 0.2));  
    pointer-events: none;  
    animation: fall 1s linear infinite;  
  }  
  
  @keyframes fall {  
    to {  
      transform: translateY(100vh);  
    }  
  }  
		#goToPageButton {  
			padding: 20px 40px; /* 增加按钮大小 */  
            font-size: 20px; /* 增加文字大小 */
            position: absolute;  
            left: 50%;  
            transform: translateX(-50%);  
            bottom: 10%; /* 调整为页面中下部分的位置 */    
            cursor: pointer;  
            background-color: transparent; /* 设置背景为透明 */  
            border: none; /* 移除边框 */  
            color: #ffffff; /* 文字颜色 */   
        }  
</style>
  </head>
  <body>
  <h1>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;<span style="color: rgba(173, 216, 230, 0.5);">&nbsp; 跟随古人脚步, 探寻西湖文化</span></h1>
    
     
    <button id="goToPageButton">走入西湖文化</button>  
    
  </body>
<script>  
  function createRain() {  
    const numDrops = 100; // 雨滴数量  
    const rainContainer = document.createElement('div');  
    rainContainer.style.position = 'fixed';  
    rainContainer.style.width = '100%';  
    rainContainer.style.height = '100%';  
    rainContainer.style.pointerEvents = 'none';  
    rainContainer.style.top = '0';  
    rainContainer.style.left = '0';  
    document.body.appendChild(rainContainer);  
  
    for (let i = 0; i < numDrops; i++) {  
      const drop = document.createElement('div');  
      drop.className = 'raindrop';  
      drop.style.left = `${Math.random() * 100}%`;  
      drop.style.animationDuration = `${1 + Math.random()}s`; // 随机动画持续时间  
      drop.style.animationDelay = `${Math.random()}s`; // 随机动画延迟  
      rainContainer.appendChild(drop);  
    }  
  }  
  
  createRain(); // 调用函数创建雨滴  
	
        // 添加按钮点击事件监听器  
        document.getElementById('goToPageButton').addEventListener('click', function() {  
            window.location.href = '分页.html'; // 替换成你想要跳转的HTML文件名  
        });  
</script>
</html>

