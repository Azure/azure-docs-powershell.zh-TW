---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 32BC6CE6-60EF-4A46-912B-8FE4FCCDF7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b91906a25d2f2d7c40f96ed07a4fd7463722023
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966983"
---
# Get-AzureSubscription

## 摘要
取得 Azure 帳戶中的 Azure 訂閱。

## 句法

### ByName (預設) 
```
Get-AzureSubscription [-SubscriptionName <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ById
```
Get-AzureSubscription [-SubscriptionId <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### 設置
```
Get-AzureSubscription [-Default] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### 當前
```
Get-AzureSubscription [-Current] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureSubscription** Cmdlet 會在您的 Azure 帳戶中取得訂閱。
您可以使用這個 Cmdlet 來取得訂閱的相關資訊，以及將訂閱傳送給其他 Cmdlet。

**AzureSubscription** 需要存取您的 Azure 帳戶。
在執行 **AzureSubscription** 之前，您必須執行 **AzureAccount** Cmdlet 或下載並安裝發佈設定檔案的 Cmdlet， ( **AzurePublishSettingsFile** 、 **Import-AzurePublishSettingsFile** 。

本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。
若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。

## 示例

### 範例1：取得所有訂閱
```
C:\PS>Get-AzureSubscription
```

這個命令會取得帳戶中的所有訂閱。

### 範例2：依名稱取得訂閱
```
C:\PS>Get-AzureSubscription -SubscriptionName "MyProdSubscription"
```

這個命令只會取得「MyProdSubsciption」訂閱。

### 範例3：取得預設訂閱
```
C:\PS>(Get-AzureSubscription -Default).SubscriptionName
```

這個命令只會取得預設訂閱的名稱。
命令會先取得訂閱，然後使用 dot 方法取得訂閱的 **SubscriptionName** 屬性。

### 範例4：取得選取的訂閱屬性
```
C:\PS>Get-AzureSubscription -Current | Format-List -Property SubscriptionName, Certificate
```

這個命令會傳回含有目前訂閱之名稱和憑證的清單。
它使用 **AzureSubscription** 命令來取得目前的訂閱。
接著，它會將訂閱的 [ **格式化清單** ] 命令，以顯示清單中選取的屬性。

### 範例5：使用替代訂閱資料檔案
```
C:\PS>Get-AzureSubscription -SubscriptionDataFile "C:\Temp\MySubscriptions.xml"
```

這個命令會從 C:\Temp\MySubscriptions.xml 訂閱資料檔案中取得訂閱。
如果您在執行 [ **載入 AzureAccount** ] 或 [匯 **入 PublishSettingsFile** ] Cmdlet 時指定了備用訂閱資料檔案，請使用 **SubscriptionDataFile** 參數。

## 參數

### -目前
只取得目前的訂閱，也就是指派為「目前」的訂閱。 根據預設， **AzureSubscription** 會在您的 Azure 帳戶中取得所有訂閱。
若要將訂閱指定為「目前」，請使用 **AzureSubscription** Cmdlet 的 **目前** 參數。

```yaml
Type: SwitchParameter
Parameter Sets: Current
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -預設值
只取得預設訂閱，也就是指派為「預設」的訂閱。 根據預設， **AzureSubscription** 會在您的 Azure 帳戶中取得所有訂閱。
若要將訂閱指定為「預設」，請使用 **AzureSubscription** Cmdlet 的 **預設** 參數。

```yaml
Type: SwitchParameter
Parameter Sets: Default
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtendedDetails
除了標準設定之外，還會傳回訂閱的配額資訊。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -設定檔
指定此 Cmdlet 讀取的 Azure 設定檔。 如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
```yaml
Type: String
Parameter Sets: ById
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionName
只取得指定的訂閱。
輸入訂閱名稱。
此值區分大小寫。
不支援萬用字元。
根據預設， **AzureSubscription** 會在您的 Azure 帳戶中取得所有訂閱。

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
您可以依名稱將輸入輸送至 **SubscriptionName** 屬性，但不能依值。

## 輸出

### WindowsAzure. 常見. WindowsAzureSubscription

## 筆記
* Get-AzureSubscription 從 **AzureAccount** 和匯 **入 PublishSettingsFile** Cmdlet 建立的訂閱資料檔中取得資料。

## 相關連結

[附加 AzureAccount](./Add-AzureAccount.md)

[AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)

[匯入-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[移除-AzureSubscription](./Remove-AzureSubscription.md)

[Set-AzureSubscription](./Set-AzureSubscription.md)


