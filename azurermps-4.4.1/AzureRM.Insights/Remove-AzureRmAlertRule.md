---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
ms.openlocfilehash: de0c1f8fa66b195452d7f2c9447189b4e925136b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453495"
---
# Remove-AzureRmAlertRule

## 摘要
移除警示規則。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Remove-AzureRmAlertRule -ResourceGroup <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzureRmAlertRule** Cmdlet 會移除警示規則。
您必須指定警示規則的名稱以及指派給它的資源群組。

## 示例

### 範例1：移除警示規則
```
PS C:\>Remove-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

這個命令會在資源群組中移除名為 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 的警示規則，預設為 [Web-CentralUS]。

## 參數

### -名稱
指定要移除之警示規則的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
指定警示規則之資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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

### [System.object]. 清單 ' 1 [AzureOperationResponse]

## 筆記

## 相關連結

[附加 AzureRmLogAlertRule](./Add-AzureRmLogAlertRule.md)

[附加 AzureRmMetricAlertRule](./Add-AzureRmMetricAlertRule.md)

[附加 AzureRmWebtestAlertRule](./Add-AzureRmWebtestAlertRule.md)

[AzureRmAlertHistory](./Get-AzureRmAlertHistory.md)

[AzureRmAlertRule](./Get-AzureRmAlertRule.md)


