---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 4EE30890-B09B-4811-88AD-4BF4FD47E431
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementNode.md
ms.openlocfilehash: ab49458426b7035a20e63ca62d86124d79291b75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449529"
---
# Get-AzureRmServerManagementNode

## 摘要
取得一或多個伺服器管理節點。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ByNodeName
```
Get-AzureRmServerManagementNode [[-ResourceGroupName] <String>] [[-NodeName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByNode
```
Get-AzureRmServerManagementNode [-Node] <Node> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmServerManagementNode** Cmdlet 會取得一或多個 Azure 伺服器管理節點。

## 示例

## 參數

### -Node
指定要取得 *ResourceGroupName* 和 *NodeName* 參數的現有節點。

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Node
Parameter Sets: ByNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NodeName
指定此 Cmdlet 取得之節點的名稱。

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定節點所屬之資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: False
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

### [ServerManagement] 的節點

## 筆記

## 相關連結

[新-AzureRmServerManagementNode](./New-AzureRmServerManagementNode.md)

[移除-AzureRmServerManagementNode](./Remove-AzureRmServerManagementNode.md)


