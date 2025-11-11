# 异步执行短耗时指令

短耗时指令指的是例如加载本地数据等指令，耗时约在 500ms 以内。

利用 setTimeout 切换异步。

```Javascript
async asyncTaskData(): Promise<string> {
  const result: string = await new Promise((resolve: Function) => {
    setTimeout(() => {
      // 执行短耗时指令
      resolve('hello, world!')
    }, 0);
  });
  return result;
}
```

注意执行指令部分的代码依然是在主线程运行，所以这个方法只用于运行短耗时指令。

# 判断代码是否在主线程运行

```Javascript
import { process } from '@kit.ArkTS';

function isMainThread(): boolean {
  return process.pid === process.tid;
}
```
