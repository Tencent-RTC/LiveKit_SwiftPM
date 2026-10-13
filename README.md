# TUILiveKit

TUILiveKit 是基于 TRTC 与即时通信 IM 的直播 UI 组件，提供主播开播、观众观看、礼物与弹幕等完整的直播场景能力，
采用状态驱动架构，可快速接入直播业务。

## 环境要求

- iOS 14.0 及以上
- Xcode 15 及以上

## 集成（SwiftPM）

1. 在 Xcode 中选择 **File → Add Package Dependencies**
2. 填入仓库地址：

```
https://github.com/Tencent-RTC/LiveKit_SwiftPM.git
```

3. 选择需要的版本（建议 `Up to Next Major Version`）
4. 在 Target 的 **Frameworks, Libraries, and Embedded Content** 中添加 product `TUILiveKit`

也可以直接写在 `Package.swift` 里：

```swift
dependencies: [
    .package(url: "https://github.com/Tencent-RTC/LiveKit_SwiftPM.git", from: "4.3.1")
],
targets: [
    .target(
        name: "YourTarget",
        dependencies: [
            .product(name: "TUILiveKit", package: "LiveKit_SwiftPM")
        ]
    )
]
```

使用时：

```swift
import TUILiveKit
```
