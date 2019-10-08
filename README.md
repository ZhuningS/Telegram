## 适用于Android的Telegram Messenger

[Telegram](https://telegram.org/)是一款注重速度和安全性的消息传递应用程序。它是超快速，简单和免费的。此存储库包含[Android Telegram App](https://play.google.com/store/apps/details?id=org.telegram.messenger)的官方源代码。

## 创建电报应用

我们欢迎所有开发人员使用我们的API和源代码在我们的平台上创建应用程序。目前，我们需要**所有开发人员**执行几项操作。

1. 为你的应用程序[**获取自己的api_id**](https://core.telegram.org/api/obtaining_api_id)。
2. 请**不要**为你的应用使用电报这个名称-或确保你的用户了解它是非官方的。
3. 请**不要**使用我们的标准徽标（蓝色圆圈中的白皮书平面）作为你应用的徽标。
4. 请阅读我们的[**安全准则，**](https://core.telegram.org/mtproto/security_guidelines)并妥善保管用户的数据和隐私。
5. 请记住也要发布**你的**代码，以符合许可要求。

### API，协议文档

电报API手册：[https](https://core.telegram.org/api)[//core.telegram.org/api](https://core.telegram.org/api)

MTproto协议手册：https://core.telegram.org/mtproto

### 编制指南

你将需要Android Studio 3.4，Android NDK版本。20和Android SDK 8.1

1. 从 https://github.com/DrKLO/Telegram ( git clone https://github.com/DrKLO/Telegram.git )下载电报源代码
2. 将你的release.keystore复制到TMessagesProj / config
3. 在gradle.properties中填写RELEASE_KEY_PASSWORD，RELEASE_KEY_ALIAS和RELEASE_STORE_PASSWORD，以访问你的release.keystore
4. 转到https://console.firebase.google.com/，创建两个应用程序ID为org.telegram.messenger和org.telegram.messenger.beta的android应用，打开firebase消息并下载google-services.json，复制到与TMessagesProj相同的文件夹中。
5. 在Studio中打开项目（请注意，应将其打开，而不是导入）。
6. 在TMessagesProj/src/main/java/org/telegram/messenger/BuildVars.java中填写值-每个变量都有一个链接，显示从何处以及从何处获取数据。
7. 你已准备好编译Telegram。

### 本土化

我们将所有翻译移至https://translations.telegram.org/en/android/。请使用它。