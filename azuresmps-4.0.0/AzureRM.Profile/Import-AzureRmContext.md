---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46efba5e2ab9a5c51172264b343b0f4f2b508065
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2019
ms.locfileid: "93442103"
---
# Import-AzureRmContext

## 摘要
從檔案載入 Azure 驗證資訊。

## 句法

### InMemoryProfile
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-WhatIf] [-Confirm]
```

### ProfileFromDisk
```
Import-AzureRmContext [-Path] <String> [-WhatIf] [-Confirm]
```

## 說明
Import-AzureRmContext Cmdlet 會從檔案載入驗證資訊，以設定 Azure 環境和內容。
您在目前會話中執行的 Cmdlet 會使用這項資訊來驗證 Azure 資源管理員的要求。

## 示例

### 範例1：從 AzureRmProfile 匯入內容
```
PS C:\> Import-AzureRmContext -AzureContext (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

這個範例會從傳遞到 Cmdlet 的 PSAzureProfile 匯入內容。

### 範例2：從 JSON 檔案匯入內容
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

這個範例會從傳遞到 Cmdlet 的 JSON 檔案選取內容。
您可以從匯入-AzureRmCoNtext 建立此 JSON 檔案。

## 參數

### -AzureCoNtext
指定此 Cmdlet 讀取的 Azure 內容。
如果您沒有指定內容，這個 Cmdlet 會從本機預設的內容讀取。

```yaml
Type: AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
指定使用 Save AzureRMCoNtext 儲存之內容資訊的路徑。

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## 輸入

### AzureRMProfile 中的 [Common.]
System.object

## 輸出

### PSAzureProfile 的設定檔。

## 筆記

## 相關連結

