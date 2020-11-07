---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 02e40cb22661d7898b9048f8e04cafdd33852994
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797530"
---
# New-AzRoleDefinition

## 摘要
在 Azure RBAC 中建立自訂角色。
提供 JSON 角色定義檔案或 PSRoleDefinition 物件做為輸入。
首先，請使用 Get-AzRoleDefinition 命令來產生比較基準角色定義物件。
然後，根據需要修改其屬性。
最後，使用此命令來建立使用角色定義的自訂角色。

## 句法

### InputFileParameterSet
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
New-AzRoleDefinition Cmdlet 會在 Azure Role-Based 存取控制中建立自訂角色。
以 JSON 檔案或 PSRoleDefinition 物件的形式，提供角色定義做為命令的輸入。
輸入角色定義必須包含下列屬性：
1) DisplayName：自訂角色的名稱
2) 描述：總結角色所准許之存取權的角色簡短描述。
3) 動作：自訂角色准許存取的一組作業。
使用 Get-AzProviderOperation 來取得可使用 Azure RBAC 加以保護的 Azure 資源提供者作業。
以下是一些有效的操作字串：
 - "*/read" 授與所有 Azure 資源提供者讀取作業的存取權。
 - "Microsoft. Network/*/read" 會針對 Microsoft. Azure 的網路資源提供者中的所有資源類型，授予讀取作業的存取權。
 - "Microsoft. Compute/virtualMachines/*" 授與所有虛擬機器及其子資源類型的所有作業的存取權。
4) AssignableScopes：一組作用域 (Azure 訂閱或資源群組) ，自訂角色就可供作業。
您可以使用 AssignableScopes，讓自訂角色只能在所需的訂閱或資源群組中使用，而不會打亂其餘訂閱或資源群組的使用者經驗。
下列是一些有效的可賦值範圍：
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e"，"/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624"：使角色可用於兩個訂閱中的作業。
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e"：使角色可在單一訂閱中供作業。
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network"：使角色只能在 [網路資源] 群組中供作業使用。
輸入角色定義可能會包含下列屬性：
1) NotActions：必須從動作中排除的一組作業，才能判斷自訂角色的有效動作。
如果您不想在自訂角色中授與存取權，您可以使用 NotActions 排除它，而不是在動作中指定該特定操作以外的所有作業。
2) DataActions：自訂角色准許存取權的資料作業集合。
3) NotDataActions：必須排除在 DataActions 中的一組作業，才能判斷自訂角色的有效資料動作。
如果您不想要在自訂角色中授與存取權的特定資料作業，請使用 NotDataActions 排除它，而不是在動作中指定該特定操作以外的所有作業。
注意：如果指派給使用者的角色指定了 NotActions 中的某個作業，而且指派另一個角色授與同一個操作的存取權，使用者就可以執行該作業。
NotActions 不是 deny 規則，這只是在需要排除特定作業時，可以輕鬆建立一組允許的作業的簡單方式。
下列是可提供為輸入 {"Name" 的範例 json 角色定義： "Description"： "可以監視所有資源，並啟動及重新開機虛擬機器"，"操作"： \[ " */read"，"Microsoft. ClassicCompute/virtualmachines/restart/動作"，" \] NotActions"： \[ "* /write" \] ，"DataActions"： \[ "microsoft. Storage/storageAccounts/blobServices/容器/blob/讀取" \] ，"NotDataActions"： "ClassicCompute" \[ \] ，"storageAccounts"： \[ "blobServices" \] }

## 示例

### 使用 PSRoleDefinitionObject 建立
```
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

### 使用 JSON 檔案建立
```
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### 所有

## 輸出

### PSRoleDefinition 中的 [.Resources.]

## 筆記
關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署

## 相關連結

[AzProviderOperation](./Get-AzProviderOperation.md)

[AzRoleDefinition](./Get-AzRoleDefinition.md)

[Set-AzRoleDefinition](./Set-AzRoleDefinition.md)

[移除-AzRoleDefinition](./Remove-AzRoleDefinition.md)

