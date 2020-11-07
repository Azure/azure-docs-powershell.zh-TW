---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 92E2409B-14BC-428F-8BAF-60D8DAFA5F57
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1adaafdfdd4331bbba86530eb532964430ed7c69
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967381"
---
# Test-AzureTrafficManagerDomainName

## 摘要
檢查是否可使用 [流量管理器] 設定檔的功能變數名稱。

## 句法

```
Test-AzureTrafficManagerDomainName -DomainName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureTrafficManagerDomainName** Cmdlet 會檢查功能變數名稱是否可做為 Microsoft Azure 流量管理器設定檔。
如果有可用的功能變數名稱，這個 Cmdlet 會傳回 $True 的值。

## 示例

### 範例1：檢查是否有可用的功能變數名稱
```
PS C:\>Test-AzureTrafficManagerDomainName -DomainName "ContosoApp.trafficmanager.net"
$True
```

這個命令會檢查是否可使用 [網功能變數名稱稱 ContosoApp.trafficmanager.net] 做為流量管理器設定檔。

## 參數

### -功能變數名稱
指定要測試的功能變數名稱。
您必須包含下列字串： 

. trafficmanager.net

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

### System.object
這個 Cmdlet 會產生 $True 或 $False。
如果有可用的功能變數名稱，這個 Cmdlet 會傳回 $True 的值。

## 筆記

## 相關連結

