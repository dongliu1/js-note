# js-note
js基础知识笔记
## 数组遍历方法
### 1、for
一般遍历数组的方法，最大值为数组长度，从下标0开始，逐个遍历
```javascript
for(let i = 0 ;i<arr.length;i++){
	//arr[i]
}
```
### 2、for of
遍历value<br/>

	1.默认
```javascript
for(let value of arr){
	//value
}
```
	2.values方法
```javascript
for(let value of arr.values()){
	//value
}
```
遍历key
```javascript
for (let key of arr.keys()){
	//key
}
```
遍历value与key
```javascript
for(let [key,value] of arr.entries){
	//key,value
}
for(let item of arr.entries){
	//item为[key,value]模式
}
```
### 3、forEach
遍历数组，函数有三个参数，item当前元素，index当前下标，array原数组
```javascript
arr.forEach(function(item,index,array){
	
})
```
### 4、find
遍历数组，返回第一个满足函数条件的数组项，不改变原数组
```javascript
arr.find(function(item,index,array){
	return item>3;
})
```
### 5、findIndex
遍历数组，返回第一个满足函数条件的数组项下标，不改变原数组
```javascript
arr.findIndex(function(item,index,array){
	return item>3;
})
```
### 6、filter
遍历数组，返回包含所有满足函数条件的数组项的新数组，不改变原数组
```javascript
arr.filter(function(item,index,array){
	return item>3;
})
```
### 7、map
遍历数组，返回按条件改变所有数组项后的新数组，不改变原数组
```javascript
arr.map(function(item,index,array){
	return item*3;
})
```
### 8、reduce
遍历数组，从左至右，按条件运算数组元素后，返回运算后所得的值。num为传入的值，可不传，若有则初始值为num。prev为之前所有数组项的计算值，current为当前数组项，index为当前数组项下标;
```javascript
arr.reduce(function(prev,current,index){
	return prev + current;
},num)；
//返回的值为num+arr[0]+arr[1]+...+arr[arr.length-1]
```
### 9、reduceRight
遍历数组，从右至左，按条件运算数组元素后，返回运算后所得的值。num为传入的值，可不传，若有则初始值为num。prev为之前所有数组项的计算值，current为当前数组项，index为当前数组项下标;
```javascript
arr.reduce(function(prev,current,index){
	return prev + current;
},num)；
//返回的值为num+arr[arr.length-1]+arr[arr.length-2]+...+arr[1]+arr[0]
```
### 10、every
遍历数组，判断数组每一项是否都满足函数条件，是则返回true，否则返回false
```javascript
arr.every(function(item,index,array){
	return item>3;
})
```
### 11、some
遍历数组，判断数组是否有一项满足函数条件，是则返回true，否则返回false
```javascript
arr.some(function(item,index,array){
	return item>3;
})
```
### 12、sort
遍历数组，按函数条件给数组排序,a为后一个数组项，b为前一个数组项
```javascript
arr.sort(function(a,b){
	return a-b;
})
//返回升序
```