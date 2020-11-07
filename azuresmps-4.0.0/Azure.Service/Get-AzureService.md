---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 86438393-8D5A-46A0-B467-6A4434E18011
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42c8760dee1aa095086d4fad3309a3a5da64b296
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967755"
---
# Get-AzureService

## 摘要
傳回包含有關目前訂閱之雲端服務之資訊的物件。

## 句法

```
Get-AzureService [[-ServiceName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## 說明
**AzureService** Cmdlet 會傳回與目前訂閱相關聯之所有 Azure 雲端服務的清單物件。
如果您指定 *ServiceName* 參數，則 **AzureService** 只會傳回相符服務的相關資訊。

## 示例

### 範例1：取得所有服務的相關資訊
```
PS C:\> Get-AzureService
```

這個命令會傳回包含所有與目前訂閱相關的 Azure 服務資訊的物件。

### 範例2：取得指定服務的相關資訊
```
PS C:\> Get-AzureService -ServiceName $MySvc
```

這個命令會傳回 $MySvc 服務的相關資訊。

### 範例3：顯示可用的方法和屬性
```
PS C:\> Get-AzureService | Get-Member
```

這個命令會顯示可從 **AzureService Cmdlet 取得** 的屬性和方法。

## 參數

### -InformationAction
指定這個 Cmdlet 回應資訊事件的方式。

此參數可接受的值為：

- 持續
- 理會
- 看
- SilentlyContinue
- 停止
- 封存

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
指定資訊變數。

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -設定檔
指定此 Cmdlet 讀取的 Azure 設定檔。
如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。

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

### -ServiceName
指定要傳回信息的服務名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

### HostedServiceCoNtext

## 筆記

## 相關連結

[新-AzureService](./New-AzureService.md)

[Set-AzureService](./Set-AzureService.md)


