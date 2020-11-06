---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
ms.openlocfilehash: 9f5927905e492fd93998e12f97a97a0380755905
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449543"
---
# Set-AzureRmRoleDefinition

## 摘要
修改 Azure RBAC 中的自訂角色。
以 JSON 檔案或 PSRoleDefinition 的形式提供已修改的角色定義。
首先，請使用 Get-AzureRmRoleDefinition 命令來檢索您要修改的自訂角色。
然後，修改您想要變更的屬性。
最後，使用此命令儲存角色定義。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### InputFileParameterSet
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
Set-AzureRmRoleDefinition Cmdlet 會更新 Azure Role-Based 存取控制中現有的自訂角色。
以 JSON 檔案或 PSRoleDefinition 物件的形式，提供更新的角色定義做為命令的輸入。
已更新的自訂角色的角色定義必須包含該角色的識別碼及所有其他必要屬性，即使它們未更新： DisplayName、Description、動作、AssignableScopes。
NotActions 是選擇性的。

下列是 Set-AzureRmRoleDefinition 的更新角色定義 json 範例

{"Id"： "52a6cc13-ff92-47a8-a39b-2a8205c3087e"，"Name"： "已更新的角色"，"描述"： "可以監視所有資源，並啟動及重新開機虛擬機器"，"動作"： \[ "*/read"、"ClassicCompute/virtualmachines/restart/action"、"/virtualmachines/start/action" \] "AssignableScopes"： \[ "/subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f" \] }

## 示例

### 使用 PSRoleDefinitionObject----------------------------------------------------更新
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/eb910d4f-edbf-429b-94F6-d76bae7ff401", "/subscriptions/a846d197-5eac-45c7-b885-a6227fe6d388")

          PS C:\> New-AzureRmRoleDefinition -Role $roleDef
```

### 使用 JSON 檔案--------------------------建立--------------------------
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## 參數

### -InputFile
包含要更新之單一 json 角色定義的檔案名。
只包含要在 JSON 中更新的屬性。
必須提供識別碼屬性。

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
角色定義物件要更新

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

### PSRoleDefinition
"Role" 是從管線接受類型 "PSRoleDefinition" 的值

## 輸出

### PSRoleDefinition 中的 [.Resources.]

## 筆記
關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署

## 相關連結

[AzureRmProviderOperation](./Get-AzureRmProviderOperation.md)

[AzureRmRoleDefinition](./Get-AzureRmRoleDefinition.md)

[新-AzureRmRoleDefinition](./New-AzureRmRoleDefinition.md)

[移除-AzureRmRoleDefinition](./Remove-AzureRmRoleDefinition.md)

