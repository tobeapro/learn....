###  Set数据结构
##### Set类似于数组，但成员都是唯一的
```javascript
	const d=new Set()
	d.add(1)
	d.add(2)
	console.log(d)
	for(var i of d){
	    console.log(i)
	}
	// Set { 1, 2 }
	// 1 2
```
``` javascript
	const d=new Set([3,4])
	d.add(1)
	d.add(2)
	d.add(3)
	d.add(4)
	console.log(d)
	for(var i of d){
	    console.log(i)
	}
	// Set { 3, 4, 1, 2 }
	// 3 4 1 2
```
##### Set的四个操作方法
- add(value)：添加某个值，返回 Set 结构本身
- delete(value)：删除某个值，返回一个布尔值，表示删除是否成功
- has(value)：返回一个布尔值，表示该值是否为Set的成员
- clear()：清除所有成员，没有返回值

##### Array.from方法可以将 Set 结构转为数组
```javascript
	const d=new Set([1,2,3,4])
	console.log(d)
    console.log(Array.from(d))
    // Set { 1, 2, 3, 4 }
	// [ 1, 2, 3, 4 ]
	// 因此可以使用Set结构达到数组去重的效果
	const arry=[1,2,1,2,3,4]
	console.log(arry)
	const d2=new Set(arry)
	console.log(d2)
	console.log(Array.from(d2))
	// [ 1, 2, 1, 2, 3, 4 ]
	// Set { 1, 2, 3, 4 }
	// [ 1, 2, 3, 4 ]
```
##### Set 结构的实例有四个遍历方法，可以用于遍历成员
- keys()：返回键名的遍历器
- values()：返回键值的遍历器
- entries()：返回键值对的遍历器
- forEach()：使用回调函数遍历每个成员

### WeakSet
##### WeakSet 结构与 Set 类似，也是不重复的值的集合,但WeakSet 的成员只能是对象，而不能是其他类型的值