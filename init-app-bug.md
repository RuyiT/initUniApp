# 初始化遇到的部分问题
## 
    1.报错 Fetching remote preset dcloudio/uni-preset-vue
    --- 解决方法：   npm config delete proxy
                    npm config set https-proxy
    2. 报错 sass-loder
    --- 解决方法：   npm install --save-dev sass-loader
                    npm install --save-dev node-sass

    3. 报错 TypeError: this.getOptions is not a function
    4. 报错 To install it, you can run: npm install --save @/static/uni.ttf
        解决：      复制hello uni-app模板里的 static的uni.ttf到本项目的static