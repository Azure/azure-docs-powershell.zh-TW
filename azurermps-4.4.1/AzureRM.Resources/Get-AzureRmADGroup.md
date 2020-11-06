---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
ms.openlocfilehash: 1079486422da769863e86d3fc16d1c3ec65d6f5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448006"
---
# Get-AzureRmADGroup

## 摘要
篩選 active directory 群組。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### EmptyParameterSet (預設) 
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SearchStringParameterSet
```
Get-AzureRmADGroup -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ObjectIdParameterSet
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
篩選 active directory 群組。

## 示例

### --------------------------使用物件識別碼篩選群組--------------------------
```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

取得含有85F89C90-780E-4AA6-9F4F-6F268D322EEE 識別碼的群組

### 使用搜尋字串----------------------------------------------------篩選群組
```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

篩選顯示名稱中含有 Joe 的所有廣告群組。

### --------------------------清單廣告群組--------------------------
```
PS C:\> Get-AzureRmADGroup
```

取得所有廣告群組

## 參數

### -ObjectId
群組的物件識別碼。

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SearchString
群組顯示名稱

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
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

### [System.object]。清單 ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6 PSADGroup]

## 筆記

## 相關連結

[AzureRmADUser](./Get-AzureRmADUser.md)

[AzureRmADServicePrincipal](./Get-AzureRmADServicePrincipal.md)

[AzureRmADGroupMember](./Get-AzureRmADGroupMember.md)

