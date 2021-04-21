---
description: 将Livefyre添加到您的本机iOS应用程序。
title: Livefyre iOS SDK
exl-id: 961c41dc-fee8-480c-a189-a20a689e705f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# Livefyre iOS SDK{#livefyre-ios-sdk}

将Livefyre添加到您的本机iOS应用程序。

使用此开放源库将Livefyre服务集成到您的本机iOS应用程序中。 Livefyre StreamHub iOS SDK基于出色的AFNetworking库，围绕我们的常见API机制提供了一个精简的层。

Livefyre还提供两个基于此SDK的iOS示例应用程序：评论流和评论范例应用程序。

## 将SDK作为Cocoa Pod集成到您的项目中（建议）{#section_qc5_h3v_zz}

将StreamHub-iOS SDK添加到项目中最便捷的方式是使用CocoaPods。 如果您没有CocoaPod，请运行宝石安装茧和窗格设置。 以下是一个Podfile示例：

```
source 'https://github.com/Livefyre/cocoapods.git' 
source 'https://github.com/CocoaPods/Specs.git' 
  
platform :ios, :deployment_target => '6.0' 
  
pod 'StreamHub-iOS-SDK', '~> 0.3.0'
```

您还需要向CocoaPod安装中添加规范存储库（这将将其克隆到`~/.cocoapods/repos`目录）：

```
pod repo add livefyre https://github.com/Livefyre/cocoapods.git
```

在应用程序项目根目录和上面添加的存储库中创建Podfile后，运行：

```
pod install
```

这将下载所有依赖项并创建一个文件MyApp.xcworkspace，您应从现在开始使用它在Xcode中打开您的应用程序项目。

## 作为Xcode子项目{#section_jcm_g3v_zz}

或者，克隆存储库：

```
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
```

接下来，将Xcode项目(LFSClient.xcodeproj)作为子项目添加到您的应用程序中（只需将LFSClient.xcodeproj文件拖入Xcode的“项目导航器”窗格即可轻松完成）。

您还需要对任何依赖项([AFNetworking](https://github.com/AFNetworking/AFNetworking)、[JSONKit](https://github.com/escherba/JSONKit))执行相同操作。

## 立即下载所有内容（不推荐）{#section_rpb_f3v_zz}

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
>要在Xcode 6中运行测试，必须在Pods-test-XCTest+OHHTTPStubSuiteCleanUp窗格[https://stackoverflow.com/a/24651704](https://stackoverflow.com/a/24651704)中向FRAMEWORK_SEARCH_PATHS添加$(PLATFORM_DIR)/Developer/Library/Frameworks。

您需要Livefyre的LFSTestConfig.plist文件，Livefyre会根据请求提供该文件。

## Xcode文档{#section_arl_b3v_zz}

您可以浏览[documentation](https://livefyre.github.com/StreamHub-iOS-SDK/)，也可以在系统上的Xcode（需要安装appledoc）中构建“文档”目标。

## 要求 {#section_m5l_13v_zz}

StreamHub iOS SDK版本自v0.2.0起要求iOS 6.0或更高版本。

## 附录（JSON支持）{#section_pcd_5hv_zz}

对于查看StreamHub-iOS SDK内部内容的用户，请注意，我们使用修改后的[JSONKit](https://github.com/escherba/JSONKit)作为默认JSON分析器（而不是Apple提供的NSJSONSerialization）。 我们必须这样做，因为Apple提供的分析器不支持解码包含整数或浮点数的JSON文件，这些整数或浮点数大于系统可以表示的整数。 我们修改的JSONKit会将非常大的数字截断到相应的系统最大值，而不是引发异常。
