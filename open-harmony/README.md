异步执行耗时指令：

利用 setTimeout 切换异步。

```Javascript
async asyncTaskData(): Promise<string> {
  const result: string = await new Promise((resolve: Function) => {
    setTimeout(() => {
      // 执行耗时指令
      resolve('hello, world!')
    }, 0);
  });
  return result;
}
```
