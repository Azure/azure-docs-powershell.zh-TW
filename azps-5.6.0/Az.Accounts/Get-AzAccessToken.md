---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 5fcd81dcfc69f020a4e17e0858abfca0edaba405
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907178"
---
# Get-AzAccessToken

## 簡介
取得原始存取權杖。 使用 -ResourceUrl 時，請確定該值與目前的 Azure 環境相符。 您可以參照到 的值 `(Get-AzContext).Environment` 。

## 語法

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

## 描述
取得存取權杖

## 例子

### 範例 1 取得 ARM 端點的原始存取權杖
```powershell
PS C:\> Get-AzAccessToken
```

取得目前帳戶 ResourceManager 端點的存取權杖

### 範例 2 取得 AAD 圖形端點的原始存取權杖
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

取得目前帳戶 AAD 圖形端點的存取權杖

### 範例 3 取得 AAD 圖形端點的原始存取權杖
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

取得目前帳戶 AAD 圖形端點的存取權杖

## 參數

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。

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
選擇性的重新配置類型名稱，支援的值：AadGraph、AnalysisServices、Arm、表示、Batch、DataLake、KeyVault、OperationalInsights、ResourceManager、Synapse。 如果沒有指定，預設值為 Arm。

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
您要求權杖的資源 URL，例如' http://graph.windows.net/ '。

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
選擇性的租使用者識別碼。如果未指定，請使用預設上下文的租使用者識別碼。

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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### 沒有

## 輸出

### System.String

## 筆記

## 相關連結
