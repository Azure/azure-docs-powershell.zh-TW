---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleDefinition.md
ms.openlocfilehash: 23bba16ea6e80d784a9de9bfb10a3a127f53b3f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452388"
---
# New-AzureRmRoleDefinition

## 摘要
在 Azure RBAC 中建立自訂角色。
提供 JSON 角色定義檔案或 PSRoleDefinition 物件做為輸入。
首先，請使用 Get-AzureRmRoleDefinition 命令來產生比較基準角色定義物件。
然後，根據需要修改其屬性。
最後，使用此命令來建立使用角色定義的自訂角色。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### InputFileParameterSet
```
New-AzureRmRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
New-AzureRmRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
New-AzureRmRoleDefinition Cmdlet 會在 Azure Role-Based 存取控制中建立自訂角色。
以 JSON 檔案或 PSRoleDefinition 物件的形式，提供角色定義做為命令的輸入。

輸入角色定義必須包含下列屬性：

1) DisplayName：自訂角色的名稱

2) 描述：總結角色所准許之存取權的角色簡短描述。

3) 動作：自訂角色准許存取的一組作業。
使用 Get-AzureRmProviderOperations 來取得可使用 Azure RBAC 加以保護的 Azure 資源提供者作業。
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

注意：如果指派給使用者的角色指定了 NotActions 中的某個作業，而且指派另一個角色授與同一個操作的存取權，使用者就可以執行該作業。
NotActions 不是 deny 規則，這只是在需要排除特定作業時，可以輕鬆建立一組允許的作業的簡單方式。

以下是可提供為輸入 {"Name" 的範例 json 角色定義： "Contoso 待命"，"描述"： "可以監視計算、網路和儲存，以及重新開機虛擬機器"，"操作"： "Microsoft. 計算//read"，"microsoft. 計算/virtualMachines/start/virtualMachines/virtualMachines"，"microsoft. 計算/ \[ */downloadRemoteDesktopConnectionFile/動作"，"Microsoft。 network/* /read"，"microsoft. storage/ */Read"，"Microsoft. 授權/* /read"，"microsoft. resources/訂閱/resourceGroups/已讀取"，"microsoft. *支援/* " \] ，"resourceGroups"： \[ "alertRules"，"AssignableScopes"： "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"，"/subscriptions/yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy" \] }

## 示例

### 使用 PSRoleDefinitionObject--------------------------建立--------------------------
```
PS C:\> $role = Get-AzureRmRoleDefinition -Name "Virtual Machine Contributor"
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
          PS C:\> $role.AssignableScopes.Add("/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e")

          PS C:\> New-AzureRmRoleDefinition -Role $role
```

### 使用 JSON 檔案--------------------------建立--------------------------
```
PS C:\> New-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## 參數

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

## 輸出

### PSRoleDefinition 中的 [.Resources.]

## 筆記
關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署

## 相關連結

[AzureRmProviderOperation](./Get-AzureRmProviderOperation.md)

[AzureRmRoleDefinition](./Get-AzureRmRoleDefinition.md)

[Set-AzureRmRoleDefinition](./Set-AzureRmRoleDefinition.md)

[移除-AzureRmRoleDefinition](./Remove-AzureRmRoleDefinition.md)

