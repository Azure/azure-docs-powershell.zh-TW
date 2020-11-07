---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
ms.openlocfilehash: 6bf44f78c763c0150e31423acd9e3594e1baa717
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791253"
---
# Get-AzRoleDefinition

## 摘要
列出所有可指派的 Azure RBAC 角色。

## 句法

### RoleDefinitionNameParameterSet (預設) 
```
Get-AzRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### RoleDefinitionIdParameterSet
```
Get-AzRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### RoleDefinitionCustomParameterSet
```
Get-AzRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
將 Get-AzRoleDefinition 命令與特定角色名稱搭配使用，即可查看其詳細資料。
若要檢查角色授與存取權的個別作業，請檢查該角色的動作和 NotActions 屬性。

## 示例

### 範例1
```
PS C:\> Get-AzRoleDefinition -Name Reader
```

取得閱讀者角色定義

### 範例2
```
PS C:\> Get-AzRoleDefinition
```

列出所有 RBAC 角色定義

## 參數

### -自訂
如果已指定，只會在目錄中顯示自訂建立的角色。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RoleDefinitionCustomParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -識別碼
角色定義 Id。

```yaml
Type: System.Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
角色定義名稱。
例如，讀取器、參與者、虛擬機器參與者。

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -範圍
角色定義範圍。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

### Guid.empty

### SwitchParameter 的系統管理功能

## 輸出

### PSRoleDefinition 中的 [.Resources.]

## 筆記
關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署

## 相關連結

[新-AzRoleAssignment](./New-AzRoleAssignment.md)

[AzRoleAssignment](./Get-AzRoleAssignment.md)

[新-AzRoleDefinition](./New-AzRoleDefinition.md)

[移除-AzRoleDefinition](./Remove-AzRoleDefinition.md)

