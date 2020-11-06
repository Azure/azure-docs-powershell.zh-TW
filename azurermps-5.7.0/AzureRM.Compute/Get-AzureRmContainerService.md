---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
ms.openlocfilehash: d2a53d221adf7483899056791aefd00b03aca26e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449950"
---
# Get-AzureRmContainerService

## 摘要
取得容器服務。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>] [<CommonParameters>]
```

## 說明
**AzureRmContainerService** Cmdlet 會取得容器服務。
您可以查看容器服務的屬性，其中包括狀態、主版和代理程式的數目，以及主要和代理程式的完整功能變數名稱。

## 示例

### 範例1：取得容器服務
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

這個命令會取得名為 CSResourceGroup17 的容器服務。

## 參數

### -名稱
指定此 Cmdlet 所取得之容器服務的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定此 Cmdlet 所取得之容器服務的資源群組。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
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

## 筆記

## 相關連結

[新-AzureRmContainerService](./New-AzureRmContainerService.md)

[移除-AzureRmContainerService](./Remove-AzureRmContainerService.md)

[更新-AzureRmContainerService](./Update-AzureRmContainerService.md)


