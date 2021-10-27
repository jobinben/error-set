

# this指向问题

1. 看代码写输出: 
   
```js
var name = 'name';
var A = {
  name: 'A',
  sayHello: function() {
      let s = () => console.log(this.name);
      return s;
  }
};
let sayHello = A.sayHello();
sayHello();
var B = {
  name: 'B'
};
sayHello.call(B);
```
tips: `ES6中的箭头函数并不会使用四条标准的绑定规则，而是根据当前的词法作用域决定this。具体来说，箭头函数会继承外层函数调用的this绑定(无论this绑定到什么)`

写输出:　``
