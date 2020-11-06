---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
ms.openlocfilehash: 07bc19bd2314164b37ec9e014f5cad68de97d21f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448248"
---
# Remove-AzureRmADServicePrincipal

## 摘要
刪除 azure active directory 服務主體。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ObjectIdParameterSet (預設) 
```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationIdParameterSet
```
Remove-AzureRmADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SPNParameterSet
```
Remove-AzureRmADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameParameterSet
```
Remove-AzureRmADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectParameterSet
```
Remove-AzureRmADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectParameterSet
```
Remove-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
刪除 azure active directory 服務主體。

## 示例

### 範例 1-依物件識別碼移除服務主體

```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

移除物件 id 為 "61b5d8ea-fdc6-40a2-8d5b-ad447c678d45" 的服務主體。

### 範例 2-依應用程式識別碼移除服務主體

```
PS C:\> Remove-AzureRmADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

移除應用程式識別碼 ' 9263469e-d328-4321-8646-3e3e75d20e76」的服務主體。

### 範例 3-依 SPN 移除服務主體

```
PS C:\> Remove-AzureRmADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

移除服務主體名稱為 "MyServicePrincipal" 的服務主體

### 範例 4-依管道移除服務主體

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzureRmADServicePrincipal
```

取得 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 Cmdlet 的物件識別碼 '」和 Remove-AzureRmADServicePrincipal 管道的服務主體，以移除該服務主體。

### 範例 5-依管道將應用程式移除服務主體

```
PS C:\> Get-AzureRmApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzureRmADServicePrincipal
```

取得應用程式識別碼 ' 9263469e-d328-4321-8646-3e3e75d20e76 ' 以及 Remove-AzureRmADServicePrincipal Cmdlet 的管道的應用程式，以移除與該應用程式相關聯的服務主體。

## 參數

### -ApplicationId
服務主體應用程式識別碼。

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationObject
要移除其服務主體的應用程式物件。

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

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

### -DisplayName
服務主體的顯示名稱。

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
如果沒有確認，請切換到刪除服務主體。

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

### -InputObject
服務主體物件。

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ObjectId
要刪除的服務主體物件識別碼。

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: PrincipalId, Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
如果已指定，則傳回已刪除的服務主體。

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

### -ServicePrincipalName
服務主要名稱。

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### Guid.empty

### System.object

### Microsoft.Azure.Graph.RBAC.Version1_6 PSADServicePrincipal
參數： InputObject (ByValue) 

### Microsoft.Azure.Graph.RBAC.Version1_6 PSADApplication
參數： ApplicationObject (ByValue) 

## 輸出

### Microsoft.Azure.Graph.RBAC.Version1_6 PSADServicePrincipal

## 筆記
關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署

## 相關連結

[新-AzureRmADServicePrincipal](./New-AzureRmADServicePrincipal.md)

[AzureRmADServicePrincipal](./Get-AzureRmADServicePrincipal.md)

[Set-AzureRmADServicePrincipal](./Set-AzureRmADServicePrincipal.md)

[移除-AzureRmADApplication](./Remove-AzureRmADApplication.md)

[移除-AzureRmADAppCredential](./Remove-AzureRmADAppCredential.md)
