# js-note
js基础知识笔记
## 数组遍历方法
### 1、for
	一般遍历数组的方法，最大值为数组长度，从下标0开始，诸葛遍历
	、、、
	for(let i = 0 ;i<arr.length;i++){
		
	}
	、、、
### 2、for of
	遍历value
	**1.默认**
	、、、
	for(let value of arr){
		
	}
	、、、
	**2.values方法**
	、、、
	for(let value of arr.values()){
		
	}
	、、、
	遍历key
	、、、
	for (let key of arr.keys()){
		
	}
	、、、
	遍历value与key
	、、、
	for(let [key,value] of arr.entries){
		
	}
	for(let item of arr.entries){
		//item为[key,value]模式
	}
	、、、
	