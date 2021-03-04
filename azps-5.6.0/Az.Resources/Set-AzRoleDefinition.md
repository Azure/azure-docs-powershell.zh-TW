---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
ms.openlocfilehash: 18488b44ff99c44d6362de68de45e81853418e0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906862"
---
# Set-AzRoleDefinition

## 簡介
修改 Azure RBAC 中的自訂角色。
以 JSON 檔案或 PSRoleDefinition 提供修改後的角色定義。
首先，使用 Get-AzRoleDefinition 命令來取回要修改的自訂角色。
然後，修改要變更的屬性。
最後，使用此命令儲存角色定義。

## 語法

### InputFileParameterSet
```
Set-AzRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
Set-AzRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
此Set-AzRoleDefinition Cmdlet 會更新 Azure 中現有的自訂角色Role-Based存取控制。
以 JSON 檔案或 PSRoleDefinition 物件提供更新的角色定義做為命令的輸入。
更新的自訂角色角色定義必須包含該角色的識別碼和所有其他必要的屬性，即使尚未更新：DisplayName、描述、動作、AssignableScopes。
NotActions、DataActions、NotDataActions 是選擇性的。
以下是適用于 Set-AzRoleDefinition { "Id"的範例更新角色定義 json："52a6cc13-ff92-47a8-a39b-2a8205c3087e"， "Name"： "Updated Role"， "Description"： "Can monitor all resources and start and restart 虛擬機器"， "Action"： \[ "*/read"， "Microsoft.ClassicCompute/virtualmachines/restart/action"， "Microsoft.ClassicCompute/virtualmachines/start/action" \] ， "NotActions"： \[ "*/write" \] ， "DataActions"： \[ "Microsoft.storage/storageAccounts/blobServices/containers/blobs/read" \] ， "NotDataActions"： \[ "Microsoft.Storage/storage"Accounts/blobServices/containers/blobs/write" \] ， "AssignableScopes"： \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }

## 例子

### 範例 1：使用 PSRoleDefinitionObject 更新
```powershell
PS C:\> $roleDef = Get-AzRoleDefinition "Contoso On-Call"
PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
PS C:\> Set-AzRoleDefinition -Role $roleDef
```

### 範例 2：使用 JSON 檔案建立
```powershell
PS C:\> Set-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
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

### -InputFile
包含要更新之單一 json 角色定義的檔案名。
只包含 JSON 中要更新的屬性。
Id 屬性為必填專案。

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -角色
要更新的角色定義物件

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### Microsoft.Azure.Commands.Resources.models.Authorization.PSRoleDefinition

## 輸出

### Microsoft.Azure.Commands.Resources.models.Authorization.PSRoleDefinition

## 筆記
關鍵字：azure、azurerm、arm、資源、管理、管理員、資源、群組、範本、部署

## 相關連結

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

[New-AzRoleDefinition](./New-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

