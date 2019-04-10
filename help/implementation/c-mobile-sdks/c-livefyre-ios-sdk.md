---
description: 将Livefyre添加到您的本机iOS应用程序。
seo-description: 将Livefyre添加到您的本机iOS应用程序。
seo-title: Livefyre iOS SDK
solution: Experience Manager
title: Livefyre iOS SDK
uuid: bfdef31a-49fc-4b25-b0 c5-300f27067302
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Livefyre iOS SDK{#livefyre-ios-sdk}

将Livefyre添加到您的本机iOS应用程序。

使用这个开放源代码库将Livefyre服务集成到您的本机iOS应用程序中。Livefyre StreamHub iOS SDK基于出色的AfNetwork库提供了围绕常用API机制的精简图层。

Livefyre还提供了两个基于此SDK的iOS示例应用程序：评论流和评论示例应用程序。

## 将SDK集成到项目中作为Cocoa窗格(建议) {#section_qc5_h3v_zz}

向项目中添加StreamHub-iOS SDK最便捷的方法是使用CoCOAPOD。如果您没有CocooAPD，请运行gem安装小样和窗格设置。下面是一个Podfile示例：

```
source 'https://github.com/Livefyre/cocoapods.git' 
source 'https://github.com/CocoaPods/Specs.git' 
  
platform :ios, :deployment_target => '6.0' 
  
pod 'StreamHub-iOS-SDK', '~> 0.3.0'
```

您还需要将规范存储库添加到您的CocooOd安装(此操作会将其克隆 `~/.cocoapods/repos` 到目录)：

```
pod repo add livefyre https://github.com/Livefyre/cocoapods.git
```

在您的应用程序项目根目录和添加的存储库中创建您的Podfile后，运行：

```
pod install
```

这将下载所有依赖项并创建MyApp. xcfeatform文件，此时您应使用该文件在Xcode中打开应用程序项目。

## 作为Xcode子项目 {#section_jcm_g3v_zz}

或者，克隆存储库：

```
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
```

接下来，将Xcode项目(LFSclient. xcodproj)添加为一个子项目(简单地将LFSclient. xcodproj文件拖动到Xcode中的Project Navigator窗格中，即可轻松完成此操作)。

您还需要与任何依赖关系([AfNetworking](https://github.com/AFNetworking/AFNetworking)、 [JSOKit](https://github.com/escherba/JSONKit))相同。

## 一次性下载所有内容(不推荐) {#section_rpb_f3v_zz}

```
cd ~/dev 
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
cd StreamHub-iOS-SDK 
git submodule init 
git submodule update 
pod repo add livefyre https://github.com/Livefyre/cocoapods.git 
pod install 
cd examples/CommentStream 
pod install 
open CommentStream.xcworkspace
```

>[!NOTE]
>
>要在Xcode中运行测试，您必须在Pod-test-XCTest+ OktptpsuiteCloudpodhttps://stackoverflow.com/a/24651704[](https://stackoverflow.com/a/24651704)中将$(TFORM_ DIR)/Developer/Library/Framework添加到Pods_ Search_ PATH中。

您需要Livefyre提供的LFestStonfig. plist文件，Livefyre可根据请求提供该文件。

## Xcode文档 {#section_arl_b3v_zz}

您可以浏览 [文档，](https://livefyre.github.com/StreamHub-iOS-SDK/) 也可以在系统中构建Xcode中的“文档”目标(需要安装Appledoc)。

## 要求 {#section_m5l_13v_zz}

StreamHub iOS SDK版本，因为v0.2.0需要iOS6.0或更高版本。

## 附录(JSON支持) {#section_pcd_5hv_zz}

对于查看StreamHub-iOS SDK内部数据的用户，请注意，我们将 [JSOKit的修改](https://github.com/escherba/JSONKit) 版本用作默认的JSON分析器(而不是Apple提供的NSjSONSerialization)。我们必须这样做，因为由Apple提供的分析器不支持解码JSON文件，这些文件包含大于可由系统表示的整数或浮点数的整数。我们的JSOKit修改版本将非常大的数字截断为相应的系统最大值，而不是引发异常。
