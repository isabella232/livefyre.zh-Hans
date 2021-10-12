---
description: 将Livefyre添加到您的本机iOS应用程序。
title: Livefyre iOS SDK
exl-id: 961c41dc-fee8-480c-a189-a20a689e705f
source-git-commit: 3091db9d7b9611e26ad65c1432856c9465694e92
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# Livefyre iOS SDK{#livefyre-ios-sdk}

将Livefyre添加到您的本机iOS应用程序。

使用此开源库将Livefyre服务集成到您的本机iOS应用程序中。 Livefyre StreamHub iOS SDK基于出色的AFNetwork库，围绕我们的常用API机制提供了一个精简的层。

Livefyre还提供了两个基于此SDK的iOS示例应用程序：评论流和评论示例应用程序。

## 将SDK作为Cocoa Pod集成到项目中（推荐） {#section_qc5_h3v_zz}

将StreamHub-iOS SDK添加到项目的最便捷方式是使用CocoaPods。 如果没有CocoaPods，请运行gem install cocoapods和pod setup。 以下是Podfile示例：

```
source 'https://github.com/Livefyre/cocoapods.git' 
source 'https://github.com/CocoaPods/Specs.git' 
  
platform :ios, :deployment_target => '6.0' 
  
pod 'StreamHub-iOS-SDK', '~> 0.3.0'
```

您还需要向CocoaPod安装中添加规格存储库（这将将其克隆到`~/.cocoapods/repos`目录）：

```
pod repo add livefyre https://github.com/Livefyre/cocoapods.git
```

在应用程序项目根目录中创建Podfile并添加上述存储库后，运行：

```
pod install
```

这将下载所有依赖项并创建一个文件MyApp.xcworkspace，您以后应该使用该文件在Xcode中打开您的应用程序项目。

## 作为Xcode子项目 {#section_jcm_g3v_zz}

或者，克隆存储库：

```
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
```

接下来，将Xcode项目(LFSClient.xcodeproj)作为子项目添加到应用程序中（只需将LFSClient.xcodeproj文件拖到Xcode的“项目导航器”窗格中即可轻松完成）。

您还需要对任何依赖项([AFNetworking](https://github.com/AFNetworking/AFNetworking)、[JSONKit](https://github.com/escherba/JSONKit))执行相同操作。

## 立即下载所有内容（不推荐） {#section_rpb_f3v_zz}

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
>要在Xcode 6中运行测试，必须将$(PLATFORM_DIR)/Developer/Library/Frameworks添加到Pods-test-XCTest+OHHTTPStubSuiteCleanUp pod[https://stackoverflow.com/a/24651704](https://stackoverflow.com/a/24651704)中的FRAMEWORK_SEARCH_PATHS。

您需要Livefyre中的LFSTestConfig.plist文件，Livefyre会根据请求提供该文件。

## Xcode文档 {#section_arl_b3v_zz}

您可以浏览[文档](https://github.com/Livefyre/StreamHub-iOS-SDK)或在系统上的Xcode中构建“文档”目标（需要安装appledoc）。

## 要求 {#section_m5l_13v_zz}

自v0.2.0以来的StreamHub iOS SDK版本需要iOS 6.0或更高版本。

## 附录（JSON支持） {#section_pcd_5hv_zz}

对于那些查看StreamHub-iOS SDK内部版本的用户，请注意，我们使用修改版的[JSONKit](https://github.com/escherba/JSONKit)作为默认JSON解析器(而不是Apple提供的NSJSONSerialization)。 我们必须这样做，因为Apple提供的解析器不支持解码包含大于系统可表示的整数或浮点数的JSON文件。 我们修改的JSONKit版本将非常大的数字截断为相应的系统最大值，而不是引发异常。
