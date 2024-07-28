## 在Web端的订单列表页面，按 F12 打开控制台，粘贴以下代码到控制台执行，自动删除订单

主要是用代码自动点击 删除和确认删除按钮

删除完后 不会自动翻页，需要手动翻页，然后再次执行代码

> taobao

```js
async function sleep() {
  return new Promise((res) => {
    setTimeout(() => {
      res();
    }, 200);
  });
}
async function task() {
  document.querySelector(".order-del").click();
  await sleep();
  document.querySelector(".btn-1.delete-order").click();
}
setInterval(task, 200);
```

> jd

```js
async function task() {
  document.querySelector(".order-del").click();
  await sleep();
  document.querySelector(".btn-1.remove-order").click();
}
async function sleep() {
  return new Promise((res) => {
    setTimeout(() => {
      res();
    }, 200);
  });
}
setInterval(task, 200);
```

tips: 欢迎补充其他网站的删除订单脚本

keywords: 订单,删除,自动,脚本,淘宝,京东,删除订单,自动删除订单,自动删除订单脚本
