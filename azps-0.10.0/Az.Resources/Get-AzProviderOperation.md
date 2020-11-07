---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: 21e1af2a36478f2e0b8e470660d0fbe2539a396e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795317"
---
# Get-AzProviderOperation

## 摘要
取得使用 Azure RBAC 安全的 Azure 資源提供者的作業。

## 句法

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
Get-AzProviderOperation 會取得 Azure 資源提供者所公開的操作。
您可以撰寫作業來建立 Azure RBAC 中的自訂角色。
此命令會以輸入操作的方式來執行作業搜尋字串 (有可能的萬用字元 ( *) 字元 (s) # A5，從而決定要顯示的操作詳細資料。使用 Get-AzProviderOperation * 來取得所有 Azure 資源提供者的所有作業。使用 Get-AzProviderOperation 的 Microsoft. 計算/* 取得所有 microsoft 的操作。計算資源提供者。

## 示例

### 取得所有提供者的所有動作
```
PS C:\> Get-AzProviderOperation *
```

### 針對特定資源提供者取得動作
```
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### 取得可在虛擬機器上執行的所有動作
```
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperationSearchString
使用可能的萬用字元 ( * ) 字元 (的操作搜尋字串) 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object
參數： OperationSearchString (ByValue) 

## 輸出

### PSResourceProviderOperation 中的 .Resources。

## 筆記
關鍵字： azure，Az，arm，資源，管理，管理員，資源，群組，範本，部署

## 相關連結
