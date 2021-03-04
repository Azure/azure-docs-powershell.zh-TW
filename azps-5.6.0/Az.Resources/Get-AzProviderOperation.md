---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: 61e38afcccccd6a96e92983d24442740351320ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917933"
---
# Get-AzProviderOperation

## 簡介
取得使用 Azure RBAC 可保護的 Azure 資源提供者的作業。

## 語法

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 描述
此Get-AzProviderOperation會由 Azure 資源提供者公開作業。
您可以撰寫作業，以在 Azure RBAC 中建立自訂角色。
該命令會使用可能的萬用字元 (輸入操作搜尋字串 () 字元 (字元) ) 決定要顯示的 *作業詳細資料。使用 Get-AzProviderOperation * 取得所有 Azure 資源提供者的所有作業。使用 Get-AzProviderOperation Microsoft.Compute/* 取得 Microsoft.Compute 資源提供者的所有作業。

## 例子

### 範例 1：取得所有提供者的所有動作
```powershell
PS C:\> Get-AzProviderOperation *
```

### 範例 2：取得特定資源提供者的動作
```powershell
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### 範例 3：取得可在虛擬機器上執行的所有動作
```powershell
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## 參數

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperationSearchString
操作搜尋字串 (包含可能的萬用字元 (*) 字元) 

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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

## 輸出

### Microsoft.Azure.Commands.Resources.models.PSResourceProviderOperation

## 筆記
關鍵字：azure、azurerm、arm、資源、管理、管理員、資源、群組、範本、部署

## 相關連結
