## HTML select option加跳转链接

### 另打开新的页面

html代码

```html
<select name="select" id="select"onchange="s_chick(this)">
    <option >友情链接</option>
    <option value="http://www.baidu.com">百度</option>
    <option value="http://www.qq.com/">腾讯</option>
</select>
```

javascript代码

```javascript
function s_chick(obj) {
        var num= 0;
        for(var i=0;i<obj.options.length;i++){
            if(obj.options[i].selected==true){
                num++
            }
        }
        if(num==1){
            var url = obj.options[obj.selectedIndex].value;
            window.open(url)
        }
    }
```

### 在当前页面跳转

html代码

```html
<select multiple="multiple" onchange="top.location=this.value;">
    
 <option value="http://www.sohu.com/">Sohu</option>
<option value="http://www.google.com/">Google</option>
</select>
```

