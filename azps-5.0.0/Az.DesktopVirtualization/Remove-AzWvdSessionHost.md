---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
ms.openlocfilehash: f7bad3a88f4d182407a90a2484daed3d538e3a69
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284735"
---
# Remove-AzWvdSessionHost

## 摘要
移除 SessionHost。

## 句法

### 刪除 (預設) 
```
Remove-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### DeleteViaIdentity
```
Remove-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 說明
移除 SessionHost。

## 示例

### 範例1：依名稱刪除 Windows 虛擬桌面 SessionHost
```powershell
PS C:\> Remove-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName
```

這個命令會刪除主機池中的 Windows 虛擬桌面 SessionHost。

## 參數

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

### -Force
[強制] 標誌，即使在 userSession 存在時，也會強制 sessionHost 刪除。

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

### -HostPoolName
指定資源群組中主機池的名稱

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
指定主機池中工作階段主機的名稱

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
在命令成功時傳回 true

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

### -ResourceGroupName
資源群組的名稱。
名稱不區分大小寫。

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
目標訂閱的 ID。

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
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

### IDesktopVirtualizationIdentity （DesktopVirtualization）的

## 輸出

### System.object

## 筆記

別名

複雜的參數屬性

若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。 如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。


INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數
  - `[ApplicationGroupName <String>]`：應用程式群組的名稱
  - `[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱
  - `[DesktopName <String>]`：指定的桌面群組中的桌面名稱
  - `[HostPoolName <String>]`：指定資源群組中的主機池名稱
  - `[Id <String>]`：資源身分識別路徑
  - `[ResourceGroupName <String>]`：資源群組的名稱。 名稱不區分大小寫。
  - `[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱
  - `[SubscriptionId <String>]`：目標訂閱的識別碼。
  - `[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱
  - `[WorkspaceName <String>]`：工作區的名稱

## 相關連結

