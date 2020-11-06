---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: B66C7A03-862A-497D-977B-1C43089DE24B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementNode.md
ms.openlocfilehash: 93efff5a9f317b7d44d071a4dd212d235df02223
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449513"
---
# Remove-AzureRmServerManagementNode

## 摘要
移除 [伺服器管理] 節點。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ByName
```
Remove-AzureRmServerManagementNode [-ResourceGroupName] <String> [-NodeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObject
```
Remove-AzureRmServerManagementNode [-Node] <Node> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzureRmServerManagementNode** Cmdlet 會移除 Azure Server 管理節點。

## 示例

## 參數

### -Node
指定此 Cmdlet 移除的節點。

您可以使用這個參數，而不是 *ResourceGroupName* 和 *NodeName* 參數。

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Node
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NodeName
指定此 Cmdlet 移除之節點的名稱。

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定節點所屬之資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
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

### 節點
形參 "Node" 接受管線中 "Node" 類型的值

## 輸出

## 筆記

## 相關連結

[AzureRmServerManagementNode](./Get-AzureRmServerManagementNode.md)

[新-AzureRmServerManagementNode](./New-AzureRmServerManagementNode.md)


