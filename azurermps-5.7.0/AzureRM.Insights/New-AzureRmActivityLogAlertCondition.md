---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
ms.openlocfilehash: d9309f2de88dc87368b510cdf6f1062d03c7f709
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449359"
---
# New-AzureRmActivityLogAlertCondition

## 摘要
在記憶體中建立新的活動記錄警示條件物件。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**新的-AzureRmActivityLogAlertCondition** Cmdlet 會在記憶體中建立新的活動記錄警示條件物件。

## 示例

### 範例1：在記憶體中建立新的活動記錄警示條件物件。
```
PS C:\>$condition = New-AzureRmActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
```

這個命令會在記憶體中建立新的活動記錄警示條件物件。

**注意** ：與此 Cmdlet 搭配使用時 Set-AzureRmActivityLogAlert 至少其中一個傳送為參數的物件，其欄位必須等於 "Category"。 否則，後端會以 400 (BadRequest。 ) 

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -等於
指定葉條件的 equals 屬性。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -欄位
指定條件的欄位。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

### ActivityLogAlertLeafCondition 中的 [管理模型]。

## 筆記

## 相關連結

[Set-AzureRmActivityLogAlert](./Set-AzureRmActivityLogAlert.md)

[Enable-AzureRmActivityLogAlert](./Enable-AzureRmActivityLogAlert.md)

[Disable-AzureRmActivityLogAlert](./Disable-AzureRmActivityLogAlert.md)

[AzureRmActivityLogAlert](./Get-AzureRmActivityLogAlert.md)

[移除-AzureRmActivityLogAlert](./Remove-AzureRmActivityLogAlert.md)

[新-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
