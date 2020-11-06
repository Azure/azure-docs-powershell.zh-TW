---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: EFBBFB60-D972-47B8-997E-B737F0CA007E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
ms.openlocfilehash: 029404938ba7a253b5130f5c807e4b66c3847d43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448007"
---
# Find-AzureRmResourceGroup

## 摘要
搜尋資源群組。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Find-AzureRmResourceGroup [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmResourceGroup** Cmdlet 會使用指定的參數搜尋資源群組。

## 示例

### 範例1：尋找所有資源群組
```
PS C:\>Find-AzureRmResourceGroup
```

這個命令會找出所有的資源群組。

### 範例2：依標記名稱尋找資源群組
```
PS C:\>Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
```

這個命令會找出所有擁有名為 testtag 的標籤的資源群組。

### 範例3：依標記名稱和值尋找資源群組
```
PS C:\>Find-AzureRmResourceGroup -Tag @{"testtag" = "testval" }
```

這個命令會找出所有名為 testtag 的標籤和值 testval 的資源群組。

## 參數

### -ApiVersion
指定要使用的資源提供者 API 版本。 如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -預先
表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
指定標記資訊（做為雜湊資料表）來篩選結果。 使用下列格式：

@ {tagName = $null} 或 @ {tagName = "tagValue"}。

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
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

### 系統管理. PSObject

## 筆記

## 相關連結

