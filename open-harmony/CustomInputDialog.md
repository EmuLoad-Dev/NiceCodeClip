```TypeScript
@CustomDialog
struct CustomDialogExample {
  controller?: CustomDialogController;
  build() {
    Column() {
      Text('我是内容').fontSize(16).margin({ bottom: 10 })
    }.onClick(()=>{
      console.log('yjf: test')
      this.controller?.close()
    })
  }
}

@Entry
@Component
struct CustomDialogUser {
  dialogController: CustomDialogController = new CustomDialogController({
    builder: CustomDialogExample(),
  })

  build() {
    Column() {
      Button('click me')
        .onClick(() => {
          this.dialogController.open();
        })
    }.width('100%').margin({ top: 5 })
  }
}
```
