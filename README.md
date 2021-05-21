## hugo + netlify 

├─content
├─public
│  ├─categories
│  ├─css
│  ├─js
│  └─tags
├─resources
│  └─_gen
│      ├─assets
│      └─images
├─static
└─themes
    └─avicenna
        ├─layouts
        │  ├─partials
        │  └─_default
        └─static
            ├─css
            └─js
###  本项目的一些细节
> 0. 本项目受ezhil和avicenna启发
> 1. 这个项目非常简约，没有任何冗余，项目简单，熟悉后可自己自由定制
> 2. 只需修改3部分即基本可以实现想要的所有效果，config.toml; main.css; layots/下的html文件
> ```{{ with .Site.Params.publications }}``` .Site 表示页面;.Params即config.toml中声明的变量; .publications即变量的属性
> ```<p class="publications"> {{ $publication.name }}, </p``` class 的属性在main.css中定义和修改
### 步骤
> 1. 本地安装hugo，配置好环境
> 2. ```hugo new set mypage``` 建立hugo空项目
├─archetypes
├─content
├─data
├─layouts
├─static
└─themes
> 3. ```git clone ...```下载hugo项目到空项目的themes, 将hugo模板的config.toml文件替换空空项目的config.toml;模板content内容复制到空文件的content中
> 4. 一般来说 hugo new post/fisrt.md 就是在content文件中建立一个post文件夹，里面放first.md;content是大多数项目的根目录
> 5. .toml文件用#注释 .yaml
> 6. ```hugo server`` 本地运行调试项目，速度更快
> 7. 跳完后运行``hugo``命令生成public文件夹；将整个项目用git上传到仓库中；用netlify启动
