> 布局内部按钮分落左右两侧中心处

```swift
// left is a boolean value
let multiplier: CGFloat = left ? 0.5 : 1.5
let constraint = NSLayoutConstraint(item: button,
                                    attribute: .centerX,
                                    relatedBy: .equal,
                                    toItem: self,
                                    attribute: .centerX,
                                    multiplier: multiplier,
                                    constant: 0)
```
