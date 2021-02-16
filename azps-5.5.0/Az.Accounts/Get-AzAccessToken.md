---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 696ae59cb5115181605b7e6e647e2eb7d2792fd8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136727"
---
# Get-AzAccessToken

## 摘要
取得原始存取權杖。 使用-ResourceUrl 時，請確定該值與目前的 Azure 環境相符。 您可能會參照的值 `(Get-AzContext).Environment` 。

## 句法

### KnownResourceTypeName (預設) 
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceUrl
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
取得存取權杖

## 示例

### 範例1取得 ARM 端點的原始存取權杖
```powershell
PS C:\> Get-AzAccessToken
```

取得目前帳戶的 ResourceManager 端點的存取權杖

### 範例2取得 AAD 圖形端點的原始存取權杖
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

取得目前帳戶的 AAD 圖形端點的存取權杖

### 範例3取得 AAD 圖形端點的原始存取權杖
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

取得目前帳戶的 AAD 圖形端點的存取權杖

## 參數

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -ResourceTypeName
選用的資源類型名稱、支援的值： AadGraph、AnalysisServices、Arm、證明、Batch、DataLake、KeyVault、OperationalInsights、ResourceManager、Synapse。 如果沒有指定，則預設值為 Arm。

```yaml
Type: System.String
Parameter Sets: KnownResourceTypeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceUrl
您正在要求權杖的資源 url，例如 " http://graph.windows.net/ "。

```yaml
Type: System.String
Parameter Sets: ResourceUrl
Aliases: Resource, ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId
選用的租使用者識別碼。如果未指定，請使用預設內容的租使用者識別碼。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### 所有

## 輸出

### System.object

## 筆記

## 相關連結
