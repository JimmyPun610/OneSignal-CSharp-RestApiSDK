![OneSignal Logo](https://onesignal.com/assets/common/logo_onesignal_color.png)
# OneSignal-CSharp
A General purpose rest ApiClient write in C# language for the OneSignal API

[![Build status](https://ci.appveyor.com/api/projects/status/ki6wuc19tx7eho36/branch/master?svg=true)](https://ci.appveyor.com/project/MundiPagg/onesignal-csharp-sdk/branch/master)

## Install via NuGet

```
PM> Install-Package OneSignal.CSharp.RestApiSDK
```

## How to use

```csharp
var client = new OneSignalClient($"{RestApiKey}");

var options = new NotificationCreateOptions();

options.AppId = $"{AppId}";
options.IncludedSegments = new List<string> { "Segment1" };
options.IncludeExternalUserIds = new List<string> { "CustomId1", "CustomId2" };
options.Contents.Add(LanguageCodes.English, "Hello world!");

client.Notifications.Create(options);
```

## OneSignal Api Oficial Documentation
[OneSignal Server API] (https://documentation.onesignal.com/reference)