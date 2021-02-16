---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 49148f1c62b71436e48b2b92a4591a7cdb36cccf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132846"
---
# Get-AzVMGuestPolicyStatus

## 摘要
取得來賓設定原則狀態 (詳細) ，以取得指派給 VM 之「來賓設定」類型的計畫。
方案是「倡議」定義類型的原則。

## 句法

### VmScope (預設) 
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeIdScope
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeNameScope
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ReportIdScope
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
Get-AzVMGuestPolicyStatus Cmdlet 會取得指派給 VM 之「來賓配置」類型之計畫的來賓設定原則狀態。
方案是「倡議」定義類型的原則。
這個 Cmdlet 會取得 VM 的相容性狀態，以及為什麼它不符合方案中個別原則的原因。

## 示例

### 範例1
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

取得 VM 所有最新的來賓設定原則狀態。
[狀態] 包含針對「來賓設定」類型的所有計劃中的每個原則的 VM 符合性狀態，遵從性原因，合規性檢查的時間，已針對合規性檢查的資源資訊。
結果包含最新狀態，不會包含先前的歷史狀態。

### 範例2
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

依計畫識別碼取得最新的來賓設定原則狀態。狀態會在計畫中包含每個原則的 VM 合規性狀態、遵從性原因、合規性檢查的時間，以及已針對合規性檢查的資源資訊。
結果不包括先前產生的狀態，它只會包含方案中每個原則的最新狀態。

### 範例3
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

依計畫名稱取得最新的來賓配置原則狀態。
狀態會在計畫中包含每個原則的 VM 合規性狀態、遵從性原因、合規性檢查的時間，以及已針對合規性檢查的資源資訊。
結果不包括先前產生的狀態，它只會包含方案中每個原則的最新狀態。

### 範例4
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

依 ReportId 取得來賓設定原則狀態。
ReportId 是 ReportId 屬性，可在 Get-AzVMGuestPolicyStatus 的結果中找到 initiativeId 或方案名稱 (請參閱其他範例) 

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

### -InitiativeId
定義類型為 [倡議] 或 [類別 is 來賓設定] 之原則的定義識別碼

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InitiativeName
定義類型為 [倡議]，類別為 [來賓設定] 的原則名稱

```yaml
Type: System.String
Parameter Sets: InitiativeNameScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportId
來賓配置原則狀態的 Id。
定義類型為「方案」和「類別是來賓設定」的原則必須指派給範圍，才能取得狀態。

```yaml
Type: System.String
Parameter Sets: ReportIdScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
資源組名稱。

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMName
VM 名稱。

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
## 輸出

### PolicyStatusDetailed 中的 GuestConfiguration。
## 筆記

## 相關連結
