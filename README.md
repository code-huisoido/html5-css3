# web移动开发
> 出处：HTML移动Web开发指南

标签（空格分隔）： html css3

---
## css3
### 6.2 选择器
<b>属性选择器</b>

- 完全匹配属性选择器
```html
    <div id="article">测试完全匹配属性选择器</div>
    <style type="text/css">
    	[id=article]{
    		color:red;
    	}
    </style>
```

- 包含匹配选择器   
```html
<div id="article">测试完全匹配属性选择器</div>
<div id="subarticle">测试完全匹配属性选择器</div>
<div id="article1">测试完全匹配属性选择器</div>
<style type="text/css">
	[id*=article]{
		color:red;
	}
</style>
```
- 首字符匹配选择器
```html
<div id="article">测试完全匹配属性选择器</div>
<div id="subarticle">测试完全匹配属性选择器</div>
<div id="article1">测试完全匹配属性选择器</div>
<style type="text/css">
	[id^=article]{
		color:red;
	}
</style>
```
- 尾字符匹配选择器
```html
<div id="article">测试完全匹配属性选择器</div>
<div id="subarticle">测试完全匹配属性选择器</div>
<div id="article1">测试完全匹配属性选择器</div>
<style type="text/css">
	[id$=article]{
		color:red;
	}
</style>
```

<b>伪类选择器</b>

- before
- after
- first-child
- last-child
- nth-child(2|even|odd)
- nth-last-child

```html
<!DOCTYPE html>
<html>
<head>
	<title></title>
</head>
<style type="text/css">
	p:before{
		content:"hello ";
	}
	p:after{
		content:"!";
	}
	p:first-child{
		color:red;
	}
	p:last-child{
		color:blue;
	}
	p:nth-child(3){
		color:yellow;
	}
	p:nth-last-child{
		color:green;
	}
	p:nth-child(even){
		font-size:2em;
	}
	p:nth-child(odd){
		font-size:1em;
	}
</style>
<body>
<p>world</p>
<p>the second word</p>
<p>the third word</p>
<p>the forth word</p>
</body>
</html>
```

### 阴影
- box-shadow
- text-shadow
```html
<!DOCTYPE html>
<html>
<head>
	<title>阴影</title>
</head>
<style type="text/css">
	div{
		/* 其他浏览器 */
		box-shadow:3px 4px 2px #000;
		/* webkit浏览器 */
		-webkit-box-shadow:3px 4px 2px #000;
		/* Firefox浏览器 */
		-moz-box-shadow:3px 4px 2px #000;
		padding:5px 4px;

		text-shadow:14px 18px 2px red;
		color:#666;
		font-size:2em;
	}
</style>
<body>
<div>shadow</div>
</body>
</html>
```

### 背景
```html
<!DOCTYPE html>
<html>
<head>
	<title>背景</title>
</head>
<style type="text/css">
	body{
		background:url("./logo.png") no-repeat;
		background-size:100px 100px;
		-webkit-background-size:100px 100px;
	}
</style>
<body>
<div>This is what I want</div>
</body>
</html>
```