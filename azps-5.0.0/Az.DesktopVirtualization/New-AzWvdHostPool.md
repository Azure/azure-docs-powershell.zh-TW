---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
ms.openlocfilehash: b91332fe8867283b5fff9cbbf1f5df96209fa2f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284752"
---
# New-AzWvdHostPool

## 摘要
建立或更新主機池。

## 句法

### CreateExpanded (預設) 
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CustomRdpProperty <String>] [-Description <String>] [-ExpirationTime <DateTime>]
 [-FriendlyName <String>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>] [-RegistrationInfoToken <String>]
 [-RegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>] [-SsoContext <String>]
 [-Tag <Hashtable>] [-ValidationEnvironment] [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### FullSenerioCreate
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-DesktopAppGroupName <String>] [-SubscriptionId <String>] [-WorkspaceName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 說明
建立或更新主機池。

## 示例

### 範例1：依名稱建立 Windows 虛擬桌面 HostPool
```powershell
PS C:\> New-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -Location 'eastus' `
                            -HostPoolType 'Pooled' `
                            -LoadBalancerType 'DepthFirst' `
                            -RegistrationTokenOperation 'Update' `
                            -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ')) `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 5 `
                            -VMTemplate $null `
                            -SsoContext $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

這個命令會在資源群組中建立 Windows 虛擬桌面 HostPool。

### 範例1：依名稱建立 Windows 虛擬桌面 HostPool
```powershell
PS C:\> New-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -Location 'eastus' `
                            -HostPoolType 'Personal' `
                            -LoadBalancerType 'Persistent' `
                            -RegistrationTokenOperation 'Update' `
                            -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ')) `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 5 `
                            -VMTemplate $null `
                            -SsoContext $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

這個命令會在資源群組中建立 Windows 虛擬桌面 HostPool。

## 參數

### -CustomRdpProperty
HostPool 的自訂 rdp 屬性。

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -描述
HostPool 的描述。

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DesktopAppGroupName
桌面應用程式群組名稱

```yaml
Type: System.String
Parameter Sets: FullSenerioCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpirationTime
註冊權杖的到期時間。

```yaml
Type: System.DateTime
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### FriendlyName
HostPool 的易記名稱。

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostPoolType
桌面的 HostPool 類型。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.HostPoolType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoadBalancerType
負載平衡器的類型。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.LoadBalancerType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -位置
資源所在的地理位置

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxSessionLimit
HostPool 的最大會話限制。

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定資源群組中主機池的名稱

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PersonalDesktopAssignmentType
HostPool 的 PersonalDesktopAssignment 類型。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PersonalDesktopAssignmentType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreferredAppGroupType
[優先] 應用程式群組類型的類型，預設為 [桌面應用程式] 群組

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PreferredAppGroupType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegistrationInfoToken
註冊權杖 base64 編碼字串。

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegistrationTokenOperation
重設權杖的類型。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RegistrationTokenOperation
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
資源群組的名稱。
名稱不區分大小寫。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -振鈴
HostPool 的響數。

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SsoCoNtext
包含 ssoCoNtext 秘密之 keyvault 的路徑。

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
目標訂閱的 ID。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
資源標記。

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ValidationEnvironment
驗證環境。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMTemplate
在 hostpool 中 sessionhosts 設定的 VM 範本。

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceName
工作區名稱

```yaml
Type: System.String
Parameter Sets: FullSenerioCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

## 輸出

### IHostPool （DesktopVirtualization）。 Api20191210Preview。

## 筆記

別名

## 相關連結

