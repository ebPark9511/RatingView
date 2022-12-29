# RatingView

A simple drag-and-drop score view.

![ezgif-6-c187b0bf831b](https://user-images.githubusercontent.com/33455020/131347961-8d7023fa-600c-4992-9218-a29312ed56a2.gif)
---

### Use
![스크린샷 2021-08-30 오후 10 28 48](https://user-images.githubusercontent.com/33455020/131348782-770cfcd6-2c7b-4a9c-b9c3-ea20dc5cb685.png)

1) Add `UIView` where you want to use it.
2) Click `UIView` and change `Custom Class` to `RatingView` in the Attributes Inspector.
3) Specify the `User defined runtime attributes` of the Attributes Inspector as required.


```Swift
// User defined runtime attributes 지정가능 옵션

// imageView 
imageName 
highlightColor
count // image의 전체 개수

//StackView
spacing
index // 초기 시작 인덱스

```



### Delegate Method

```Swift
// RatingView Delegate Method
 
protocol RatingViewDelegate: AnyObject {
    func didChangeIndex(_ index: Int)
}
 
```

### Swift Package Manager

The [Swift Package Manager](https://swift.org/package-manager/) is a tool for automating the distribution of Swift code and is integrated into the `swift` compiler. 

Once you have your Swift package set up, adding Alamofire as a dependency is as easy as adding it to the `dependencies` value of your `Package.swift`.

```swift
dependencies: [
    .package(url: "https://github.com/ebPark9511/RatingView.git", .upToNextMajor(from: "1.0.0"))
]
```


### Etc
- `constraint` is calculated as `content size` when `width` of `RatingView` and `priority` of `height` is set to `low (250)`.
