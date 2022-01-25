```js
//1.键值对去重
// Object键值对
//var array = [{value: 1}, {value: 1}, {value: 2}];
function unique(array) {
    var obj = {};
    return array.filter(function(item, index, array) {
        return obj.hasOwnProperty(typeof item + JSON.stringify(item)) ? false : (obj[typeof item + JSON.stringify(item)] = true)
    })
}
//2.数组去重
//var mm = [1,2,1]
function unique(array) {
    return Array.from(new Set(array))
}
//3.正则匹配手机号
function checkPhone() {
    if (!(/^1[345678]\d{9}$/.test(phone))) {
        alert("手机号码有误，请重填");
        return false;
    }
}
//4.邮箱验证
var pattern = /^([A-Za-z0-9_\-\.\u4e00-\u9fa5])+\@([A-Za-z0-9_\-\.])+\.([A-Za-z]{2,8})$/;
//邮箱正则表达式
this.emailReg = /^\w+([-+.]\w+)*@\w+([-.]\w+)*\.\w+([-.]\w+)*$/;

//排除数组里是否含有某个键值对 有就删除 没有就添加
// var trackObj1 = {
//     "trackId": 31,
//     "direcLine": "line31"
// };
// var currentTrack = [];
// currentTrack.push(trackObj1);
// var trackObj2 = {
//     "trackId": 30,
//     "direcLine": "line30"
// };
// currentTrack.push(trackObj2);
if (index == -1) {
    this.dblclickArr.push({
        deviceId: oNode.deviceId,
        name: oNode.name
    });
    //有就删除
} else {
    this.dblclickArr.splice(index, 1);
}
// 5.判断currentTrack这个数组中是否存在trackId=31的对象
/*按照属性值，查找对象*/
function findElem(arrayToSearch, attr, val) {
    for (var i = 0; i < arrayToSearch.length; i++) {
        if (arrayToSearch[i][attr] == val) {
            return i;
        }
    }
    return -1;
}
var index = findElem(currentTrack, "trackId", "31");

// 6.for循环存在异步的处理方式
var i = 0;
run();

function run() {
    console.log('这是第' + i + '次循环------------------------');
    console.log('在这做什么事情，比如你的ajax请求');
    console.log('请求回来了，数据有了，处理中...');
    console.log('接下来判断是否要进行下一次循环');
    if (i < 10) {
        i++;
        run();
    } else {
        console.log('循环完事了！');
    }
}
let str = '2,3';
console.log(str[0]);

//7.对象数组去重
var obj = {};
var aa = [{
    "name": "aa",
    "pwd": "xvxv"
}, {
    "name": "aa",
    "pwd": "xvxv"
}, {
    "name": "bb",
    "pwd": "xvxv"
}, {
    "name": "cc",
    "pwd": "xvxv"
}];

aa = aa.reduce(function(item, next) {
    console.log(item, next, next.name, obj[next.name])
    obj[next.name] ? '' : obj[next.name] = true && item.push(next);
    return item;
}, []);
console.log(aa);

//特殊转译
let index = res.data.routerDetail.search(`\\\\`);
this.topContent = res.data.routerDetail.substring(0, index);
this.bottomContent = res.data.routerDetail.substring(index + 2);

// 8.复杂实现(一个参数)
// 原理: clone(o) = new Object; 返回一个对象
// 递归函数

function clone(o) {
    var temp = {};
    for (var key in o) {
        if (typeof o[key] == 'object') {
            temp[key] = clone(o[key]);
        } else {
            temp[key] = o[key];
        }
    }
    return temp;
}
// 9.返回顶部的通用方法
function backTop(btnId) {
    var btn = document.getElementById(btnId);
    var d = document.documentElement;
    var b = document.body;
    window.onscroll = set;
    btn.style.display = "none";
    btn.onclick = function() {
        btn.style.display = "none";
        window.onscroll = null;
        this.timer = setInterval(function() {
            d.scrollTop -= Math.ceil((d.scrollTop + b.scrollTop) * 0.1);
            b.scrollTop -= Math.ceil((d.scrollTop + b.scrollTop) * 0.1);
            if (d.scrollTop + b.scrollTop == 0)
                clearInterval(btn.timer, (window.onscroll = set));
        }, 10);
    };

    function set() {
        btn.style.display = d.scrollTop + b.scrollTop > 100 ? "block" : "none";
    }
}
backTop("goTop");

// 10.检测URL链接是否认有效
function getUrlState(URL) {
    var xmlhttp = new ActiveXObject("microsoft.xmlhttp");
    xmlhttp.Open("GET", URL, false);
    try {
        xmlhttp.Send();
    } catch (e) {} finally {
        var result = xmlhttp.responseText;
        if (result) {
            if (xmlhttp.Status == 200) {
                return true;
            } else {
                return false;
            }
        } else {
            return false;
        }
    }
}

//   11. 返回指定字符长度文字内容换行
let str = "8001-实验OSN25001/10-Q1SL4-1|123321hhjljs阿斯蒂芬"

function show(s) {
    var re = '';
    var length = s.length;
    for (var i = 0, j = 1; i < length; i++, j++) {
        re += s[i];
        if (j && j % 14 == 0) {
            re += '\n';
        }
    }
    return re;
}
console.log(show(str));

//12 去除括号以及括号内的内容
let aa = "234(123)ddd(555)";
let bb = (aa.replace(/\(.*?\)/g, ''));
console.log("bb", bb);
```
