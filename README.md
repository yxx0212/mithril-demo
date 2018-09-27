> 任何具有 view 方法的 JavaScript 对象都是 Mithril 组件。组件可以用过 m() 函数调用

## 一、如何创建组件

### 1. 对象字面量

- *Step1 - 定义组件对象*

  ```js
  var Button = { /* stuff */ }
  ```

- *Step2 - 为组件添加 view() 方法*

  ```js
  var Button = {
    view: function(){ /* stuff */ }
  }
  ```

### 2. 原型链

```js  
var Progress = function(){ /* stuff */ }
Progress.prototype.view = function(){ /* stuff */ }
Progress.prototype.onInit = function(){ /* stuff */ }
Progress.prototype.onCreate = function(){ /* stuff */ }
```

  ### 3. 类

```js
class Switch {
  view(){ /* stuff */ }
}
```  

## 二、如何使用组件

```js
m.mount(element, new Switch);
m.render(element, m(new Switch));
m.route(element, '/', {
  '/home': new Switch
});
```
