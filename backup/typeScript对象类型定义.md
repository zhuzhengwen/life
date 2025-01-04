**对象类型**
 ```typescript
// The parameter's type annotation is an object type
function printCoord(pt: { x: number; y: number }) {
  console.log("The coordinate's x value is " + pt.x);
  console.log("The coordinate's y value is " + pt.y);
}
printCoord({ x: 3, y: 7 });
 ```
两个属性的类型注释了参数 - x 和 y - 均为 number 型。你可以使用 , 或 ; 来分隔属性，不指定类型就会假定为any类型


**可选属性**
 ```typescript
function printName(obj: { first: string; last?: string }) {
  // ...
}
// Both OK
printName({ first: "Bob" });
printName({ first: "Alice", last: "Alisson" });
 ```
在函数入参名字后加入? ，相当于定义该属性不是非必须的，类似java的有参构造器。
注意点，如果该属性不存在需要进行undefined判断



<!-- ##{"timestamp":1546307280}## -->