---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/update-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
ms.openlocfilehash: 223884fb5974c94b31d8d3ddf2017e1c6e3740b4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917253"
---
# Update-AzSapMonitor

## 簡介
針對指定的訂閱、資源群組和監視器名稱修補 SAP 監視器的標記欄位。

## 語法

### UpdateExpanded (預設) 
```
Update-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### UpdateViaIdentityExpanded
```
Update-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 描述
針對指定的訂閱、資源群組和監視器名稱修補 SAP 監視器的標記欄位。

## 例子

### 範例 1：根據名稱更新 SAP 監視器
```powershell
PS C:\> Update-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01 -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

這個命令會以名稱更新 SAP 監視器。

### 範例 2：根據物件更新 SAP 監視器
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Update-AzSapMonitor -InputObject $sap -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

這個命令會按物件更新 SAP 監視器。

## 參數

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。

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

### -InputObject
身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
SAP 監視器資源的名稱。

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
資源組的名稱。

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。
訂閱識別碼會構成每個服務通話 URI 的一部分。

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -標記
資源的標記欄位。

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -確認
執行 Cmdlet 之前，提示您確認。

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
顯示 Cmdlet 執行時會發生什麼情況。
不會執行 Cmdlet。

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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.models.IHanaOnAzureIdentity

## 輸出

### Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.models.Api20200207Preview.ISapMonitor

## 筆記

別名

複雜的參數屬性

若要建立下列描述的參數，請建構包含適當屬性的雜湊表。 有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。


INPUTOBJECT： <IHanaOnAzureIdentity> 身分識別參數
  - `[Id <String>]`：資源識別路徑
  - `[Location <String>]`：已刪除的儲存庫位置。
  - `[OperationKind <AccessPolicyUpdateKind?>]`：作業名稱
  - `[ProviderInstanceName <String>]`：提供者實例的名稱。
  - `[ResourceGroupName <String>]`：資源組的名稱。
  - `[ResourceName <String>]`：身分識別資源的名稱。
  - `[SapMonitorName <String>]`：SAP 監視器資源的名稱。
  - `[Scope <String>]`：資源的資源提供者範圍。 受管理身分驗證擴充的父資源。
  - `[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。 訂閱識別碼會構成每個服務通話 URI 的一部分。
  - `[VaultName <String>]`：儲存庫的名稱

## 相關連結

