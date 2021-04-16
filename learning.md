* AWSAccessKeyId=AKIATHR3I2BR7RCYLHGO
* AWSSecretKey=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


css : inline internal  external
* Tag selectors： h1{collor:red}
* Class selectors: .bacon{}
* ID selectors: #heading{}  id是只有一个，独一无二

* 16px = 100% = 1em  = 1rem  
* font-size 最好的处理方式是用rem 继承累加大小   但是90px  static性质没有累加性

**Common inline elements**
* <span> <img> <a>
**common block elememnts**
* <p> <h1> <div> <ol> <ul> <li>  <form> 
* 一旦使用position
* : sbsolute  就不再是block

**display**
* block
* inline
* inline-block
* none

**margin**
* 两个数是    上下   左右    
* 三个数    上   左右  下
* 四个数     上  右 左  下

**Bootstrap 的链接要放在最开始**

**z-indx 必须有设定 position 才能有效**

**关于综合命令：**
* div#title  没有父子关系，就是寻找条件筛选，带着title id 的div,  
* div #title   父子关系，div设定了寻找范围， div 中所有带title  id的elements.

**Selector 优先级**
越 specification 越优先
ID > class > 后面的 > 前面的

# JavaScript

* ""  quotation   double quotes     single quotes
* ;  semi-colon
* ()  round brackets   curly brackets

* typeof() 显示类型

cmmand + k   to clear screen

> **slice(1,5)**
系统会在位置1前面和位置5前面切。

* .toUperCase() 
* .toLowerCase()
* .length   
* .slice()
* Math.floor()    run down number
* Math.pow(a,b)    数字a的b平方
* Math.round(a);    四舍五入最接近的数字
* Math.random();     1 > 数字 >= 0
* ===   equal   >=
* !--    is not equal to
* &&  and
* ||  or

**array**
* guestList.includes()    检查list 里有没有  返回true false
* .push();   add new item to array
* .pop;   it takes the last item in the array and remove it from the array.

**properties**
* innerHTML = " "
* style
* firstChild

**Methods**
* click()
* appendChild()
* setAttribute()

**关于抽取网页内容**
* document.getElementsByTagName("");
* document.getElementsBYClassName("");
* document.getElementById("");
* document.querySelector("li a"); li.item 综合以上三个功能  需要带上 # . 符号    ； 只返回第一个符合条件的值。
* document.querySelectorAll("#list .item");
zdocument.getElementsByTagName("li")[2].style.color = "purple";
* 所有抽取值不止一个的，都可以用[ ]来确定。
----
* document.querySelector("button").classList.add("invisible).  atttach an classList to the elements selected         invisible 就加进了button class 里面
*  document.querySelector("button").classList.remove("invisible).
*  document.querySelector("button").classList.toggle("invisible).
----
  **.innerHTML   vs    .textContent**
* document.querySelector("h1").innerHTML;   抽取的是h1 tag  包含的所有内容，可以编辑HTML符号。
* docuemnt.querySelector("h1").textContent;   抽取的是纯文本

**Manipulate attributes**
* document.querySelector("a").attributes;  显示attributes attached to the element
* document.querySelector("a").getAttribute("href");
* document.querySelector("a").setAttribute("href","https://www.bing.com");

**在网页写javascript**
* debugger;今天debugger mode
  
  **Higher Order Function**
  * function thais is able to take functions as inputs

**Callback function**
* function that gets passed in as an input

# jQuery
* $("h1");    document.querySelector("h1");
* google cdn

**JavaScript 引用要放到底格body上面  jQuery 放在javaScript 上面** 
```javascript
* $("h1").addClass("big-title margin-50");
* $("h1").removeClass("big-title margin-50");
* $("h1").css("color","red");
*  $("h1").hasClass("big-title margin-50"); 返回一个boolean
*  $("h1").text("Click me");
*  $("h1").html("<em>hello</em>");
```
**manipulate attribute**

```javascript
*  $("img").attr("src");   console.log($("img").attr("src");)  get the value of the attribute
*  $("a").attr("href","https://www.yahoo.com");    set the value of the attribute
```

**adding event listeners with jQuery**
```javaScript
$("h1").click(function(){
  $("h1").css("color","purple");
});

$("button").click(function(){
  $("h1").css("color","purple");
});

$("input").keydown(function(event){
  console.log(event.key)
});

$("body").keydown(function(event){
  console.log(event.key)
});

第二种add listener的方法
$("h1").on("mouseover",function(){
  $("h1").css("color","red");
})
```
**Adding and Remvoing Elements with jQuery**
```javaScript
$("h1").before("<button>New</button>");     after  prepend  append

// 点击 button 然后显示 和 不显示
$("button").on("click",function(){
  $("h1").toggle();    // fadeIn  fadeOut  slideUp slideDown  slideToggle()
})


("button").on("click",function(){
  $("h1").slideUp().slideDown().animation({opacity: 0.5});   形成动画
})

//得到event 的 id
$(".btn").on("click",function(event){
       
    var user = event.target.id;
});

// 一段时间去掉加入的效果
  setTimeout(function () {
    $("#" + currentColor).removeClass("pressed");
  }, 100);

  // setTimeout
  setTimeout(function(){$("body").css("background-color","#011F3F");},100);
```

# Unix Command
* kernel: 就是果仁； refers to the actual program that interfaces with the hardware so it's the core of the operating system,
* shell:  就是果皮；  the user interface for you as a human to be able to interact with the kernel and in turn with the hardware of your computer.
* graphical user interface VS command line interface
* bash shell = Bourne Again Shell    is    CLI(command line interpreter) for UNIX system.
* ls   列出文件  
* cd   change directory   
* cd desktop    进入desktop
* cd ~     回到root directory
* cd ..    返回上一级
* ctrl + a    光标移动到最前端
* ctrl + e    光标移动到最后端
* ctrl + u    clear the current line
* mkdir  Darcy  新建文件夹
* touch Text2.txt   新建file
* open Text2.txt    open file
* open -a Atom Text2.txt    用某软件打开文件
* rm Text2.txt       删掉文件
* pwd         find path 
* rm *       delete all in the directory
* rm -r Darcy/   delete directory
* mv  源文件  目标文件       移动文件
*  sudo  super user do
*  **node index.js**   用node 来运行javascript文件  

# Node.js
```javascript
const fs = require("fs");

fs.copyFileSync("file1.txt","file2.txt");
```
* 在terminal 点击  node  进入
* .exit  退出  
* ctrl + c 退出processes
* REPL: Read Evaluation Print Loop
* NPM: node package manager  command line: npm init   建立这个package  然后去npmjs.com 上去下载各种库
  

  # express
  * 安装设置网上都有
* npm install express 
```javascript
const express = require('express')
const app = express()
const port = 3000

app.get('/', function(req, res){
  res.send('Hello World!')
})

app.listen(port, function() {
  console.log(`Example app listening at http://localhost:${port}`)
})
  ```
  * 一定要 命令行  node server.js 执行之后才能打开网页
  *  nodemon  安装可以自动运行node.js 不需要每次都手动运行  
  *  sudo npm install -g nodemon
  *  nodemon  server.js
  *  **要post 需要安装body-parser      command line: npm install body-parser**
  *  app.use(bodyParser.urlencoded({extended: true}));

**API**
* ampersand sympol: &
* API : application programming interface is a set of commands , functions, protocols and objects that programmers can use to create software or interact with an external system.
* endPoint   信息的来源地址 就是endpoint
* Paths :     endpoint + branch          
* Parameter :   endpoint + branch + ? + key + query
* JSON : JavaScript Object Notation    JSON.stringify(); JSON.parse()
* XML : extensible markup language
* HTML : Hyper Text Markup language
token:
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


# Git & GitHub
* git status  
* git stash
* git log
* git diff chapter3.text   比较目前chapter3.text 和最近的 save point 的 chapter3.text 的区别。
* git checkout chapter3.text    roll back to the last version chapter3.text committed
* git remote add origin https://git.........   添加remote          
* git push -u origin master   上传 origin is the name of remote     master is the name of branch
* git rm --cached -r .  get all files out of staging area 
* .gitignore        #评论  pound sign      * 
* copy 资源   /gitignore
* git clone https://.....
* git branch darcy-plot  建立新branch
* git branch   查看branch 的信息
* git checkout darcy-plot   进入branch
* git merge darcy-plot     merge branches
* git add . -p  add并且有显示不同
* git rm --cached ./file.txt
  
* git config --global --list

**Change remote origin**
* git remote set-url origin new.git.url/here
  **branch**
* git checkout -b new-feature 建立并且进入新branch
* git branch -d new-feature  删除branch
* git config --global --list

**commit 之后  可以  git rm temp.text    git commit -m "" 这个文件就不TRACKING了,彻底删掉了**
**git history 插件的使用":si  shift+command+P**
**Undoing things**
* git restore --staged <file>  从stage里取消文件
* git reset <commit> README.md  彻底去掉这个commit


**git stash**
* git add .
* git stash    把一个不确定要不要上传的文件暂存一下，这个文件会从vs 里消失
* git stash -m '名字'   给git stash 取一个名字 
* git stash list
* git stash pop 把暂存的文件提取出来,弹出最上面的stash,这个stash就消失了
* git stash apply [--index]   这个可以拿出特定的stash，这个stash仍然存在。

**git clean -f**  //新建的文件, 尚未add的， 全部删掉

**revert**
*  git log   // 找到commit ID copy
* git revert 加上拷贝的ID  它会产生一个新的commit
* git reset  会还原，但是完全删掉，不能用

  **merge**
* 一定要处在 receiving 的位置上
* merge 冲突解决后 要进行 add  commit

**rebase vs  merge** rebase 原来的线全部删掉，变回单线结构，但是保留所有的开发记录， merge后不保留开发记录

**git diff**
* test1.txt在修改后，未add 的情况下
* git  diff test1.txt    // 查看修改的情况
* git checkout test1.txt   // test1.txt 还原到未修改前的状态了
* git checkout .   // 整个目录都还原回去了



  ----d

# EJS
* let : block scope and no init     var  globally , function, locally scope and has init       const 约等于 let  只是是个常量，不能改变。     

## node.js 文件初始化
* npm init
* npm i express body-parser 
* npm i ejs
* npm i mongoose
* npm i lodash
  
**Node.js 标准的基本设置 可复制**
```javascript
const express = require("express");
const bodyParser = require("body-parser");
const https = require("https");
const mongoose = require("mongoose");
const _ = require("lodash");
const ejs = require("ejs");
const encrypt = require("mongoose-encryption");

var app = express();

const port = 3000;

app.use(bodyParser.urlencoded({extended:true}));
app.use(express.static("public"));
app.set("view engine", "ejs");

app.get("/",function(req,res){
   res.send("Hello");
})

app.listen(port, function () {
    console.log("Server started on port 3000");
  })

```

**关于JavaScript string 的处理有关library  lodash**
* npm i lodash
* const _ = require("lodash");



# SQL

update  tablename  set    where
* :wq!   save and exit 

# mongoDB shell
* 用 homebrew 安装配置mongoDB 非常简单
* mongod 启动service 
* mongo   进入mongo shell
* show dbs  显示所有的数据库
* db      显示目前所在数据库
* us fruit   switch to fruit db
* db.products.insertOne({_id:1, name:"pen", price: 1.20}) 建立一个products的表 并且插入一条记录
* show collections    显示有多少表格
* db.products.find()    db.products.find({name: "Pencil"})   显示表格内容
* db.products.find({price: {$gt: 1}}) 大于1块钱的东西  find item
* db.products.find({_id:1},{name:1})    返回 name  这个field
* db.products.updateOne({_id: 2}, {$set:{stock:32}})   update item
* db.products.deleteOne({_id:2})        delete item
* 如果忘了退出mongoDB  sudo pkill -f mongod
* db.dropDatabase（）  删掉目前所在的db
* db.lists.drop() 删掉collection



# mongooes
* npm i mongoose 
* npm i    新下载的文件的module 全部安装
```javascript
const mongoose = require("mongoose");

mongoose.connect("mongodb://localhost:27017/todolistDB",{useNewUrlParser:true,useUnifiedTopology: true})

const itemsSchema = {
  name: String,
};

const Items = mongoose.model( "Items", itemsSchema);

const item1 = new Items ({
  name: "Welcome to do your list"
});

item1.save(function(err){
    if(!err){
             res.send("Successfully added a new article.")
         }else{
             res.send(err);
         }
})

const item2 = new Items ({
  name: "Hit the + button to add a new item."
});

const item3 = new Items ({
  name: "Welcome to do your list"
});

const defaultItems = [item1,item2, item3];

Items.insertMany(defaultItems,function (err) {
     if(err){
       console.log(err);
     }else{
       console.log("Successfully saved default items to DB.");
     }
  })
```
## Heroku
* terminal 进入 app 文件夹，  git init
*  git add .
*  git commit -m "asdf“
*  heroku login
*  输入密码
*  heroku create
*  touch Procfile
*  vim Procfile     添加内容  web: node app.js
*  修改port
  
```javascript
let port = process.env.PORT;
if (port == null || port == "") {
  port = 3000;
}
  app.listen(port, function() {
  console.log("Server started on port 3000");
});
```
* 查出自己node 版本  node --version  添加到package.json  licence 下面
```javascript
  "engines": {
    "node": "14.15.4"
  },
```
* 在app文件夹建立 .gitignore 文件，并且编辑
```javascript
/node_modules
npm-debug.log
.DS_Store
/*.env
```
* 重新 add commit
* git push heroku master

**REST**
* REST: REpresentational State Transfer
* https: http securie
* %20 http url 代表 空格

**cookie and session**
npm i passport passport-local passport-local-mongoose express-session

OAuth: Open authorisation

to help to make google api work
*  npm i mongoose-findorcreate  

**React.js**
* plugin :     sublime-babel-vscode
* create React APP :   
* npx create-react-app my-app
* cd my-app
* npm start

map vs forEach    区别就是map 自动返回一个array  而forEach 需要先建立一个array 往里push

```javascript
var numbers=[1,12,34,45];
// filter
const newNumbers = numbers.filter(function (num){
  return num <10;
});
// reduce  -accumulate a value by doing something to each item in an array 
let newNumber = numbers.reduce(function(accumulator, currentNumber){
    return accumulator + currentNumber;
})
// find    -find the first item that matches from an array
let newNumber = numbers.find(num => num > 10);
})
// findIndex  - find the index of the first item that matches.
let newNumber = numbers.findIndex( num => num > 10);
})

substring()
```
**一些有用的JavaScript命令**
```javascript
setInerval(updateTime, 1000);
const now = new Date().toLocaleTimeString();
const [time, setTime] = useState(now);

```

# Full-Stack shills
**React.js 是csr 还是ssr**

**session storage  vs   local storage :**
* session storage:   payment用session. 不需要储存用户信息的情况， 关掉tab,信息就没了， 同一个URL不显示一样的信息。     
*  local storage: 需要储存用户的信息， 如facebook 不能每次打开一个页面重新登录一次。 关掉tab/browser 信息都在， 除非信息过期。同一个URL显示同样 的信息。
*  cookie: 用的越来越少，存在电脑里，怕virus.
* Whenever a document is loaded in a particular tab in the browser, a unique page session gets created and assigned to that particular tab. That page session is valid only for that particular tab.
* A page session lasts as long as the tab or the browser is open, and survives over page reloads and restores.
* Opening a page in a new tab or window creates a new session with the value of the top-level browsing context, which differs from how session cookies work.
* Opening multiple tabs/windows with the same URL creates sessionStorage for each tab/window.
* Closing a tab/window ends the session and clears objects in sessionStorage.

**SPA :** single page application. is a web application or website that interacts with the user by dynamically rewriting the current web page with new data from the web server, instead of the default method of the browser loading entire new pages. The goal is faster transitions that make the website feel more like a native app.

A single-page application is an app that works inside a browser and does not require page reloading during use. You are using this type of applications every day. These are, for instance: Gmail, Google Maps, Facebook or GitHub.no page reloads, no extra wait time. It is just one web page that you visit which then loads all other content using JavaScript — which they heavily depend on. 

SPA is fast, as most resources (HTML+CSS+Scripts) are only loaded once throughout the lifespan of application. Only data is transmitted back and forth.

SPA can cache any local storage effectively. An application sends only one request, store all data, then it can use this data and works even offline.

**ssr csr** 
* server-side render: Is method or concept when HTML is build on server. 服务端产生HTML返回到浏览器。 Search engine optimization (SEO). Next.js
Perceived performance
* csr:  HTML is build on the browser. javascript 产生html   没法看到网站详细内容，不能用于marking的网站

Suppose, you want to share a link on social networking site, which reads the information from your link and the content on that link is dynamic then you must go for SSR rather than CSR

**http  vs  https**
1. Safer websites
2. Sense of trust
3. Improve SEO
4. Simplified Integration

**jason:** JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is easy for humans to read and write. It is easy for machines to parse and generate.

**ssh**

**DOM :** document Object Model

**网络数字含义**
200 OK
400 Bad Request
401 Unauthorized
402 Payment Required
403 Forbidden
404 Not Found
500 Internal Server Erro

# 2 HTML
**标签 除了 <strong>  <small> </small>   <span> 其他一概不用**
**UL   OL**

box 

float： 图文并排的时候用flot
.box1{
  box-shadow: 2px(水平偏移) 10px(垂直偏移) 5px(模糊度) red;
}

The box-sizing property allows us to include the padding and border in an element's total width and height.

如果用width 和 height  定义box, ling-height 的值设定和height相等可以让内容上下居中，但是用padding就无所谓了。

图片不能超过250K。

如果定义height  max-height and height:100%

loading time request: Sprite sheet, Img compress

Interview Question
• Position: absolute relative
• Animation
• Flex
Copy
• Animation ,Box shadow, Border-radius, padding , margin , Font-size, color, background color
Don’t copy:
• flex , block, inline-block , float

border-box tells the browser to account for any border and padding in the values you specify for an element's width and height. If you set an element's width to 100 pixels, that 100 pixels will include any border or padding you added, and the content box will shrink to absorb that extra width

**Lesson5CSS**
npm install sass -g

sass style.scss style.css  因为html只能引用css，所以我们把scss转化成css
sass --watch style.scss style.css  无缝衔接编译css 

node package manager

**Lesson6 Javascript**
变量提升 面试
传参数的时候， 数组是引用，但是数字是copy.
访问object   obj.name  obj["name"]   有空格或者有变量let key = "name";时候应该用数组

构造function 名字用大写；

car2 = Object.assign({},car); 这个是完全复制一份object

-768-1280-   做好三个尺寸的responsive 就好

space-between 适用于左边是图片，右边是文字

width  或者max-width 默认就是100%。  或者 % 不能写死   图片有可能大超出，所以可以用maxwidth， 文字可以%。    有时候两者配合着用，让文字图片不要相互挡着
height: auto

**Lesson 10 Node.js**
BOM : browser object  Model
DOM : document object model
javascript object : 

shell: terminal 的执行环境
nvm   npm

echo $SHELL   查看你是什么shell
shell session  不同shell 同系统不同回话是独立的  分时操作系统


nvm install 
nvm use 
nvm alias default    三个记住就行

**REPL :** Read-Eval-Print-Loop

**重点 ：**
* port 端口号 是操作系统的概念，在操作系统上，任何一个程序想要和别的网络程序进行通讯，必须监听操作系统的某一个端口，才能暴露出去。
* 非https   默认端口80   https 默认端口443
* tcp 通过ip 和端口建立连接， 通讯内容是http协议的内容，http 是建立在tcp协议之上的内容
* http: hypertext transfer protocol
* shema + host + past
* curl 是永远承担client 角色


**使用npm**
* npm init
* npm install koa
* npm info koa
* npm i koa -D    放在dev dependecies
* npm install --production    production envrionment  不安装dev dep
* npm prune --production      delete all dev dependency










cursor pointer 

# lesson 11 Agile
* SDLC    software development life cycle 
* Envision / design / build / stabilize / deploy / production support / end of life
* 

buffer: 进阶
cluster: 轻度了解  一段代码理解就可以
events 重点掌握  扩展阅读design pattern
file system: 重要 读文件和写文件   和linux 一样
global : 掌握
http:理论知识 : 报文协议  header  常见header   header的具体含义   respons code的含义 
url: 重点掌握  
modules commonJS modules : 了解
os： 查询时候看一下就行 
path： 重点掌握
process： 重点掌握
querrystring :   querystring.parse("a=1&b=2");  string to json    querystring.stringfy(); json to string

timer : 掌握

utility: 类型判断  各种工具 轻度了解


421182 1987 1107 1020

kill -9 709   停止709进程    kill只是负责传送信息， -9是杀掉进程

#!/Users/darcyxian/.nvm/versions/node/v14.16.0/bin/node
chmod a+x ./process.js   增加这个文件的执行权限 可以直接执行

mv process.js add.js    重新命名
export 环境变量
shebang

# full-stack react
**ES6**
* Javascript(Vanilla, ES6)
* ECMAScript
* this  谁调用指向谁 没有调用body this就是undefined
* RMR  readable  Maintainable reusable       能不写if else就不写  能用=>尽用     决不能用 ctrl c / cmd c， 只要用了就说明代码不好
* 箭头函数是为了解决this 的问题
* 标签模板用不到
* 数组解构是由顺序一一对应， 但是object 是key 来解构一一对应。 解构就是语法糖
* 短路计算  
* 函数的执行本质就是call   fn()实际是简写了， 它原本样子应该是是 fn.call(undefined)   fn(123) b本质就是 fn.call(undefined, 123); 第一个参数总是他自己 也就是this   也就是谁调用this就指谁
  ```js
    const obj = {
      name:'aa',
      fn:function(){
        console.log(this)
      }
    }
   obj.fn();
   // 实质是
   obj.fn(obj)
   // js 里面调用方法都是把自己作为<第一个>参数给传进去，所以this 就指向这个obj

   fun（）;
   // 这种情况就是没有调用方，第一个参数就是undefined


  ```
* 单行的时候  react 可以省略return
* class  写成 className   for 写成 htmlFor
* children 是保留字段 自动默认为children
* 自己定义的component要用首字母大写方式命名  所有html element 是小写的  这样可以区分
* 面试 jsx的基本工作原理？
* 面试 为什么有jsx 的地方一定会有react？
* 面试 为什么出现jsx?
* jsx 是facebook 为了更加方便书写React而开发的， 而react本身是不包括JSX的
* 计算机只认识汇编，8进制01
* 把human readable 代码, 转换成Machine Readable代码， 就是compile
* Babel.js  ： non ES stander -> ES stander, complier
* Facebook, React 只是扩展了compiler， make babel 能够编译 jsx
* 都放在文件夹里面
* webpack ： bundle your scripts  打包工具  就是让各种import的关系建立起来
* npm : 管理所有JavaScript依赖
* react babel loader  加到webpack.config.js里面 这样可以在打包的同时顺便编译。
* webpack.config.js
  ```javascript
    const path = require('path'); // node 环境与浏览器环境的区别  node必须用require
                                  // react 需要 webpack 打包的东西都用import

    module.exports = {
      entry: './main.js',
      output:{
        path: path.resolve(__dirname, 'dist'),
        filename: 'bondle.js'
      },
    };

  ```
### 配置webpack
#### webpack  就是用来生成一个bundle.js 文件，来给index.html引用，表示component里面层层依赖的路径。java 自带这个不需要。
* 1 npm init   npm install webpack  
*  建立webpack.config.js
```javascript
const path = require('path');

module.exports = {
  entry: './main.js',
  output: {
      // 找到相对路径，产生一个dist 文件夹，产生一个bundle，js文件
    path: path.resolve(__dirname, 'dist'),
    filename: 'bundle.js',
  },
};
```
* 2 修改package.json文件de scripts   package.json里面name script 最重要 
```javascript
scripts: {"build":"webpack --config ./webpack.config.js --mode development"}
```
* 3 安装babel-loader   npm install babel-loader   npm install @babel/core     npm install @babel/preset-react   要装不少东西  在webpack.config.js添加module
注意里面presets这一项改为preset-react
  ```javascript
   module: {
    rules: [
      {
        test: /\.m?js$/,
        exclude: /(node_modules|bower_components)/,
        use: {
          loader: 'babel-loader',
          options: {
            presets: ['@babel/preset-react']
          }
        }
      }
    ]
  }
  ```
* 4 npm install webpack-cli
* 5 输出的dist 文件夹中的bundle.js 要写到html底部进行引用。
* 6 npm run build   开始运行  根据错误安装各类东西
* 
* 7 html webpack plugin（自动给index.html添加dist/bundle.js的引用）：    npm install --save-dev html-webpack-plugin
* 8 clean webpack plugin: npm install --save-dev clean-webpack-plugin  (如果你变更了webpack.config.js 里面的filename，改成了bundle2.js，react会创建一个新的bundle2.js， 这个plugin会自动删掉老的bundle.js)

```javascript
 const HtmlWebpackPlugin = require('html-webpack-plugin');
 const { CleanWebpackPlugin } = require('clean-webpack-plugin');
 // webpack.config.js
plugins:[
  new HtmlWebpackPlugin({
    template:'./index.html',
  }),
  new CleanWebpackPlugin(),  // 自动清理改变budle 文件后，多余出来的老文件
]
```

* 9 webpack css loader     // main.js import css
* npm install css-loader style-loader     然后在webpack.config.js里面module rules里面添加下面
```javascript
     {
        test: /\.css$/i,
        use: ["style-loader", "css-loader"],
      },
``` 
* 10 webpack img loader:   npm install file-loader --save-dev  // 在webpack.config.js里面module rules里面添加下面
```javascript
 {
        test: /\.(png|jpe?g|gif)$/i,
        use: [
          {
            loader: 'file-loader',
          },
 }
``` 
* 11 React 引用本地图片注意 import  src={}
* 12 webpack dev server   热部署  npm install --save-dev webpack-dev-server
```js
webpack.config.js
  devServer: {
    contentBase: './dist',
  },

  package.json
  "start": "webpack serve --open"
```
* 13 设置react sass： npm install sass-loader sass webpack --save-dev
* 14 npm install node-sass   npm install sass   npm install style-loader   npm install postcss-loader   
* 15 npm install autoprefixer    // autoprefixer 是实际执行postcss 安装-webkit 增加网站的兼容性。
```js
// 新建一个postcss.config.js     postcss-loader 会自动去寻找这个文件
module.exports = {
    plugins:[
        require('autoprefixer')
    ]
}
```
* 
* sass-loader   postcss-loader  css-loader  style-loader  从下到上  选择性
``` js
// webpack.config.js 的简易模板 
const path = require('path');
const HtmlWebpackPlugin = require('html-webpack-plugin');
const { CleanWebpackPlugin } = require('clean-webpack-plugin');

module.exports = {
    mode: 'development',
    entry: {
        app: path.join(__dirname,  'main.tsx')
    },
    target: 'web',
    resolve: {
        extensions: ['.ts', '.tsx', '.js']
    },
    module: {
        rules: [
            {
                test: /\.tsx?$/,
                use: 'ts-loader',
                exclude: '/node_modules/'
            },
            {
                test: /\.m?js$/,
                exclude: /(node_modules|bower_components)/,
                use: {
                  loader: 'babel-loader',
                  options: {
                    presets: ['@babel/preset-react']
                  }
                }
            },
            {
                test: /\.css$/i,
                use: ["style-loader", "css-loader"],
            },
            {
                test: /\.(png|jpe?g|gif)$/i,
                use: 
                  {
                    loader: 'file-loader',
                  },
            },
            {  // 关于sass 的设置，
                test: /\.s[ac]ss$/i,
                use: [
                  // Creates `style` nodes from JS strings
                  "style-loader",
            
                  "css-loader",
                  // Translates CSS into CommonJS
                  "postcss-loader",  // css-loader  改成 postcss-loader  可以自动加上-webkit 增加兼容性
                  // Compiles Sass to CSS
                  "sass-loader"
                ],
          }
        ]},
    output: {
        filename: 'bundle.js',
        path: path.resolve(__dirname, 'dist')
    },
    plugins: [
        new HtmlWebpackPlugin({
            template: path.join(__dirname, 'index.html')
        }),
        new CleanWebpackPlugin(),  // 自动清理改变budle 文件后，多余出来的老文件
    ],
    devServer: {
        contentBase: './dist',
      },

}

// json
{
  "name": "testtypescript",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "build": "webpack --config webpack.config.js",
    "start": "webpack serve --open"
  },
  "author": "",
  "license": "ISC",
  "dependencies": {
    "autoprefixer": "^10.2.5",
    "react": "^17.0.2",
    "react-dom": "^17.0.2"
  },
  "devDependencies": {
    "@babel/core": "^7.13.13",
    "@babel/preset-react": "^7.13.13",
    "@types/react": "^17.0.3",
    "@types/react-dom": "^17.0.3",
    "@types/webpack": "^5.0.0",
    "babel-loader": "^8.2.2",
    "clean-webpack-plugin": "^3.0.0",
    "css-loader": "^5.2.0",
    "file-loader": "^6.2.0",
    "html-webpack-plugin": "^5.3.1",
    "postcss-loader": "^5.2.0",
    "sass": "^1.32.8",
    "sass-loader": "^11.0.1",
    "style-loader": "^2.0.0",
    "ts-loader": "^8.0.18",
    "typescript": "^4.2.3",
    "webpack": "^5.28.0",
    "webpack-cli": "^4.5.0",
    "webpack-dev-server": "^3.11.2"
  }
}

```
* create React App   
* 1 ESLint  检查代码正确的工具 自己不想配置可以直接下载airbnb eslint， 用airbnb的标准配置； 2 学会typescript ；   3 husky 工具: 强制性得帮助团队控制代码质量，如果不能通过单元测试，不能commit; 4 editorconfig.org  把编译器的统一起来;  5 jest 前端测试  6 运行typescript项目 create-react-app name template --typescript
* Typescript: .ts     
  ```typescript
  const num: number = 10;
  const str: string = 'sdf';
  const num: boolean = true;
  const num: undefined = undefined;
  const obj = {
    a: 10,
    b: 'abc'
  }
  const obj:{a:number b?:number} {  // 加问号是说明这个属性可以有，也可以没有
    a: 10,
    b: 10
  }
  const obj:{[key in string]: string}{ // 要求key 和 值都要是string

  }
  const obj:Record<string,string> = { // 和上面一样的简单写法

  }
  const fn = （a: number, b: number）: number  => {   // 第三个number是返回值类型
    retrun a - b;
  }
  let xxx: (a: number)=> boolean // boolean 是返回值

  // 定义类型模式
  type Xxx ={
    a: number,
    b: string,
  }

  const obj: xxx ={

  }
  // interface 同样可以继承
  interface Base {
   a: number;
  }
  interface Ojb extends Base{
    b: string
  }
  const ddd: Obj = {
    a: 'string',
    b: 10,
  }
 
  <input onChange={handleOnChange}/>

  handlerOnChange = (event:ReactEvent<HTMLInputElement>) => { // HTMLButtonElement
    event.target.value
  }

  // 泛型

  // T 可以继承 type   这个区别于interface 的一点是 fn必须说明 a:number
  type Obj = {
    a: number
  }

  const fn = <T extends Obj> (a: T) => {
    return a;
  }
  fn<{a:number, b: string}>({
    a: 10, b: 'ad' })


  const fn = <T> (a: T) => {
    return a;
  }
  fn<number>(2);
  fn<Record<string, string>>({a: 'sfasf'});  //Record 对象类型


  // props 怎么用type 
  type Props ={
    a: number,
    b?: string
  }
  const Component = (props : Props) => {
   const {a,b} = props;
    return <div>Hello World {a} {b}</div>
  }
  <Component a={10} b={'xxx'} />
  
  ```

# Lesson 14 React 哲学3  （state） and tutorial
* import {} from....   It basically just allows you to import a single member if you require. In the case you provided it may not be as useful as other ones. For example:
```javascript
// constants.js
export const TEST_CONST = 'HOLA';
export const OTHER_TEST_CONST = 'YO';

// someFile.js
import { TEST_CONST } from './constants';

console.log(TEST_CONST); // output: 'HOLA'
```

* Javascript 基础数据类型: number, boolean, string, undefined, null, object, symbol
* async await / pormise / 宏任务+微任务 / setTimeout
* setTimeout()  倒数计时，我想在多久之后执行什么  会返回一个定时器的id 
  ```javascript
  const id = setTimeout(()=>{console.log(2)}, 2000);
  clearTimeout(id);

  setInterval()
  ```
*  Promise   三种状态 pending  fulfilled  reject
*  promise.then() 这个回调是优先回调， 优先于setTimeout();
*  new Promise（） 是立刻执行
*  async await 是promise的语法糖
  ```javascript
    new Promise((resolve,reject) =>{
      // 我要执行一些东西 发起网络请求
      if(网络请求陈宫)
      resolve();
      else
      reject();
    })
    // 成功的回调函数
    const fetchDataFormAPI = () => {
      return 123;
    }

    const promise = new Promise((resolve,reject)=>{
        setTimeout(()=>{
      // 成功拿到了函数 123
      const dataFromWeb = fetchDataFromAPI();
       resolve(dataFromWeb);
    }, 3000);
    });
    promise.then((data) =>{
       console.log(data); //123  data 就是拿到了 这个 123
      return new Promise((resolve, reject) => {
        setTimeout(() => {
          const dataFromWeb = fetchDataFromAPI();
          resolve(dataFromWeb);
        }, 3000)
      }).then(data => {
        console.log(data);
      })
    });
    
    // 失败的回调函数
    const promise = new Promise((resolve,reject) =>{
      setTimeout(() => {
        reject('失败的原因')
      },3000)
    })
    // 注意这then里面有两个fn, 顺序不能变，固定的第一个是成功的，第二个是失败的
    promise.then((data)=>{
      console.log(data);
    }),(reason)=>{
      console.log(reason); // 运行结果显示string  '失败的原因'
    }
   
   123   abc
   成功的数据是[123,abc]
   Promise.all([promise1,promise2]).then(成功，失败)   // 这个作用的就是所有的在数组里promise 都会执行， 但是只有所有的都成功了，才能成功回调，否者就是失败回调。
   Promise.race([promise1,promise2]).then(成功，失败) // 谁先成功了，谁就成功回调
    
  ```
  * SPA: Single Page Application 
  * HTML: 最初是作为美国军方分享文档使用。
  * event.preventDefault();  click 本来就是默认要页面跳转 但是这个就是阻止了它 跳转
  * javascript: pass by reference vs pass by value   当function 接受的是一般类型时候，copy value, 当接受的的object时候，传递的是地址。
  * javascript: class component   VS  function component
  * css-in-js   styled-components
  
  *  react 要多写 dummy component   少写 smart component
  *  只有 html element 是有 event binding
  *  半本秘籍： 1 single responsibility 2 dependency injection 3 1/2 open close    外加 PMR
  *  react state  state就是一个plain javascript object,用来保存可更改的状态， 替换掉obj 和 各种reference更新。
  *  setState 已经封装了render方法。它作用是 更改state + 触发render
  * 没有caller 的fn 严格模式下是undefined，非严格模式window
  * webpack 打包是严格模式
  * 在构造器中，this 永远是正确指向。  
  * 绑定this, 并替换原有function    this.changePage = this.changePage.bind(this); 
  * 箭头函数的this 永远指向最初定义时候的this 
  * 在前端性能中，性能瓶颈是DOM Paint, DOM Paint 是非常消耗性能的。
  * React async state update
  * this.setState(obj,callback2) object 会异步更新， cb2会在 state update 成功后被调用
  * this.setState(cb1,cb2) cb1 会回传这次更新前的上次 state, cb2会在update成功后调用。
  * 作业： 1 react p1 更新到简历  2 p2  更新到简历  3 不带api 的p3 
 ```js
  this.setState({
    count: this.state.count + 1;
  }, ()=>{
    console.log(this.state.count);
  });

  this.setState((prevState) => {
    return {
      count: prevState + 1,
    }
  }, ()=>{
    console.log(this.state.count);
  });
 ```



  ```
  Basic style
  - Typographic
  - Enhancement

  Boxing
  - margin
  - padding
  - border

  Layout
  - FlexBox
  - Position

  layout -> boxing -> basic style
  ```

# 21 Java Basic
大型网站技术构架   微服务设计


OR:  object relational database
DAO: data access object      每一个object  就是一个数据库的table
每一个 microService  对应一个独立的 database
ALB: application load balance
statefull: store session in server    login
stateless: not store session in server
JWT: json web token
raddis: 

数组查找很快 但是插入和删除就很慢
链表插入删除很快 但是查找很慢 因为它要从头一个一个找

#  23 
如果有参数的constructer， 不定义空参数的默认constructer的话，默认constructer就失效了，都定义了的话不会失效。

scss module 要研究一下

javascript fatigue

javascript 运行环境  browser   node.js
null 是人为代表没有
let 不会变量提升
```js
const person3 = {...person2} // ... 展开符
‘32’ == 32 true // == 不做类型比较 只比较里面的数值
person2 === person1 // 复杂数据类型 === 是比较数据    

lodash 提供了很多功能
git

// 看array   object    

```

# 28 SQL
ddl dml
```sql

CREATE TABLE directors (
  director_id SERIAL Primary key,
	first_name varchar(30),
	last_name varchar(30) not null,
	date_of_birth DATE,
	nationality varchar(20)
)

CREATE TABLE examples (
   example_id serial primary key,
	first_name varchar(30),
	last_name varchar(30)
)

alter table examples
add column email varchar(50) unique;

DROP TABLE examples;

```
# 27 
* docker-compose up   // 运行docker 配置
* docker ps -a  // 列出所有的docker image
*  docker volume ls  // 列出所有的volume
*  docker contianer ls // 列出所有的container


