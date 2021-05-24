# See https://hellouniapp.dcloud.net.cn/pages/component/scroll-view/scroll-view 内置组件库
# See https://uniapp.dcloud.io/component/README 官方文档
# See https://www.cnblogs.com/xiaohuochai/p/7372665.html animate使用案列
# See https://www.jianshu.com/p/74c06e649e71 当 uni-app 遇见 vscode
# See https://blog.csdn.net/fangkang7/article/details/110085522 微信端运行
# See https://developers.weixin.qq.com/miniprogram/dev/api/ 微信开发者工具文档

# 创建项目
    1. vue create -p dcloudio/uni-preset-vue ‘项目名’
    2. 选择hello uni-app模板 （用来拷贝部分代码块）
    3. 另行新建一个需要的真正项目，选择默认模板 
    4. 安装组件语法提示 ---npm i @dcloudio/uni-helper-json
    
# app.vue 引入全局公共样式

## 引入样式库
    uni.css     ---官方ui库,从hello uni-app里common组件拷贝到此项目的common文件夹里（需新创建）
    animate.css     ---css动画库    
                    从官网下载 https://raw.github.com/daneden/animate.css/master/animate.css
    icon.css        ---图标库
                    fontclass方式 将线上链接的代码copy到icon.css ,然后在用的地方加 <iconfont类名 + ‘class类名’>
    common.css      ---公共样式库
                    从https://raw.github.com/daneden/animate.css/master/animate.css拷贝到animate.css 或
                    直接 npm install animate.css --save
                    使用： 看官方效果 加class类名 “animate__animated animate__bounce” 以新版本animate__开头

## 设置全局样式
    1. 页面高度100%,默认字体28upx,默认行高1.8
    ```
    page {
        height: 100%;
        font-size: 28upx;
        line-height: 1.8;
        background: #fff;
    }
    ```
    2. 图片默认100%宽度
    ```
    image {
        width: 100%;
    }
    ```
    3. 主色调
    ```
    /* 主背景颜色（橙色） */
    main-bg-color {
        background: #FD6801;
    }
    /* 主点击背景颜色（淡橙色） */
    main-bg-hover-color {
        background: rab(253,104,1,0.85);
    }
    /* 主字体颜色（橙色） */
    main-text-color {
        background: #FD6801;
    }
    /* 主边框颜色（橙色） */
    main-border-color {
        background: #FD6801;
    }
    ```

## pages.json配置
   1. 全局配置 globalStyle
   2. 底部导航 tabBar
        从阿里图标库搜首页> 输入颜色#878787> 输入大小80> 下载PNG格式放置static里面（包括一个选择的一个没选中的）
        ```
        "tarBar": {
            // 字体颜色
            "color": "#B1B1B1",
            // 选中的颜色
            "selectedColor": "FD6801",
            // 边框的颜色
            "borderStyle": "black",
            // 背景颜色
            "backgroundColor": "#ffffff",
            // 导航列表
            "list": [
                {
                    "pagePath": "pages/index/index",
                    "iconPath": "static/tabbar/index.png",
                    "selectedIconPath": "static/tabbar/index.png",
                    "text": "首页"
                }
            ]
        }
        ```
    3. 首页配置 app-plus
        ```
        "app-plus":{
					 "scrollIndicator":"none",//隐藏滚动条
					 "bounce":"none",//关闭反弹效果
					 "titleNView":{
						 // 搜索框配置
						 "searchInput":{
							 "align":"left",
							 "backgroundColor":"#F7F7F7",
							 "borderRadius":"4px",
							 "placeholder":"智能积木 越野四驱车",
							 "placeholderColor":"#CCCCCC",
							 "disabled":true
						 },
						 //配置按钮
						 "buttons":[
							 // 左边
							 {
								 "color":"#999999",
								 "colorPressed":"#BBBBBB",
								 "float":"left",
								 "fontSize":"22px",
								 "fontSrc":"/static/font/iconfont.ttf",
								 "text":"\ue67a"
							 },
							 // 右边
							 {
								 "color":"#999999",								 
								 "colorPressed":"#BBBBBB",
								 "float":"right",
								 "fontSize":"22px",
								 "fontSrc":"/static/font/iconfont.ttf",
								 "text":"\ue661"
							 }
						 ]
					 }
				 }
        ```

## 常用样式封装
    common里面的zcm-main.css代码解读
    1.  颜色 - 背景颜色 - 边框颜色 - 文本颜色
    2.  布局
    3.  边框
    4.  内边距  
    5.  外边距
    6.  字体大小   
    7.  行高
    8.  flex布局

## 组件开发
    -. components
        -. common   全局公共组件
        -. index    首页组件


