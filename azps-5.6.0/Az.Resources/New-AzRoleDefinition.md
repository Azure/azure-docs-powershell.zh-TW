---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 0930b66cf12d9c96d4fe00fa823cfd67c87081f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907537"
---
# New-AzRoleDefinition

## 簡介
在 Azure RBAC 中建立自訂角色。
提供 JSON 角色定義檔案或 PSRoleDefinition 物件做為輸入。
首先，使用 Get-AzRoleDefinition 命令來產生比較基準角色定義物件。
然後，根據需要修改其屬性。
最後，使用此命令使用角色定義來建立自訂角色。

## 語法

### InputFileParameterSet
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
Cmdlet New-AzRoleDefinition在 Azure 中建立自訂角色Role-Based存取控制。
提供角色定義做為 JSON 檔案或 PSRoleDefinition 物件的命令輸入。
輸入角色定義必須包含下列屬性：
1) DisplayName：自訂角色的名稱
2) 描述：角色的簡短描述，摘要說明角色授予的存取權。
3) 動作：自訂角色授予存取權的操作集。
使用Get-AzProviderOperation取得 Azure 資源提供者的作業，這些提供者可以使用 Azure RBAC 進行安全保護。
以下是一些有效的運算字串：
 - "*/read" 會授予所有 Azure 資源提供者讀取作業的存取權。
 - "Microsoft.Network/*/read" 會授予 Azure Microsoft.Network 資源提供者中所有資源類型讀取作業的存取權。
 - 「Microsoft.Compute/virtualMachines/*」會授予虛擬機器及其子資源類型之所有作業的存取權。
4) 可指派的Scope：Azure 訂閱 (或資源群組) 自訂角色可供指派的一組範圍。
您可以使用 AssignableScopes，讓自訂角色僅可供需要指派的訂閱或資源群組使用，而且不會干擾其餘的訂閱或資源群組的使用者體驗。
以下是一些有效的可指派範圍：
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e"， "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624"：讓角色可在兩個訂閱中指派。
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e"：讓角色可在單一訂閱中指派。
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network"：讓角色只能在網路資源群組中指派。
輸入角色定義可能包含下列屬性：
1) NotActions：您必須從動作排除的作業集，以決定自訂角色的有效動作。
如果您不想將自訂角色的存取權授予特定作業，使用 NotActions 來排除該作業並不方便，而不是在動作中指定該特定作業外的所有作業。
2) DataActions：自訂角色授予存取權的資料作業集。
3) NotDataActions：一組必須排除在 DataActions 中的作業，以決定自訂角色的有效資料動作。
如果您不想將自訂角色的存取權授予特定資料作業，使用 NotDataActions 來排除它，而不是在動作中指定該特定作業外的所有作業，是方便的。
注意：如果使用者獲指派角色，指定 NotActions 中的作業，同時指派另一個角色以授予相同作業的存取權，使用者將可以執行該作業。
NotActions 不是拒絕規則，只要排除特定作業，它就是建立一組允許作業的便利方式。
以下是範例 json 角色定義，可做為輸入 { "Name"： "Updated Role"， "Description"： "Can monitor all resources and start and restart virtual machines"， "Actions"： \[ "*/read"， "Microsoft.ClassicCompute/virtualmachines/restart/action"， "Microsoft.ClassicCompute/virtualmachines/start/action" \] ， "NotActions"： \[ "*/write" \] ， "DataActions"： \[ "Microsoft.storage/storageAccounts/blobServices/containers/blobs/read" \] ， "NotDataActions"： \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \] ， "AssignableScopes"： \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }

## 例子

### 範例 1：使用 PSRoleDefinitionObject 建立
```powershell
PS C:\> $role = Get-AzRoleDefinition -Name "Virtual Machine Contributor"

PS C:\> $role.Id = $null
PS C:\> $role.Name = "Virtual Machine Operator"
PS C:\> $role.Description = "Can monitor, start, and restart virtual machines."
PS C:\> $role.Actions.RemoveRange(0,$role.Actions.Count)
PS C:\> $role.Actions.Add("Microsoft.Compute/*/read")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/start/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/restart/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/downloadRemoteDesktopConnectionFile/action")
PS C:\> $role.Actions.Add("Microsoft.Network/*/read")
PS C:\> $role.Actions.Add("Microsoft.Storage/*/read")
PS C:\> $role.Actions.Add("Microsoft.Authorization/*/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/resources/read")
PS C:\> $role.Actions.Add("Microsoft.Insights/alertRules/*")
PS C:\> $role.Actions.Add("Microsoft.Support/*")
PS C:\> $role.AssignableScopes.Clear()
PS C:\> $role.AssignableScopes.Add("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

PS C:\> New-AzRoleDefinition -Role $role
```

### 範例 2：使用 JSON 檔案建立
```powershell
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
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
包含單一 json 角色定義的檔案名。

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -角色
角色定義物件。

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### 沒有

## 輸出

### Microsoft.Azure.Commands.Resources.models.Authorization.PSRoleDefinition

## 筆記
關鍵字：azure、azurerm、arm、資源、管理、管理員、資源、群組、範本、部署

## 相關連結

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

[Set-AzRoleDefinition](./Set-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

