---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
ms.openlocfilehash: 51229c966c0e4c8b0ec74c3c940037aca5081b15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625454"
---
# Get-AzureRmProviderOperation

## 摘要
取得使用 Azure RBAC 安全的 Azure 資源提供者的作業。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
Get-AzureRmProviderOperation 會取得 Azure 資源提供者所公開的操作。
您可以撰寫作業來建立 Azure RBAC 中的自訂角色。
此命令會以輸入操作的方式， (中使用萬用字元 ( * ) 字元 (s) # A5，決定要顯示的操作詳細資料。

使用 Get-AzureRmProviderOperation * 來取得所有 Azure 資源提供者的所有作業。

使用 Get-AzureRmProviderOperation 的 Microsoft. Compute/* 來取得 Microsoft 的所有操作。計算資源提供者。

## 示例

### 取得所有提供者的所有動作
```
PS C:\> Get-AzureRmProviderOperation *
```

### 針對特定資源提供者取得動作
```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### 取得可在虛擬機器上執行的所有動作
```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

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

### -OperationSearchString
使用可能的萬用字元 ( * ) 字元 (的操作搜尋字串) 

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 字串
"OperationSearchString" 參數從管線接受類型 "String" 的值

## 輸出

### PSResourceProviderOperation 中的 .Resources。

## 筆記
關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署

## 相關連結
