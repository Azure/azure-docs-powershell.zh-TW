---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/invoke-azcostmanagementexecuteexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementExecuteExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementExecuteExport.md
ms.openlocfilehash: 752af43a72151296c4c90ecc32923a786c7b4081
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277459"
---
# Invoke-AzCostManagementExecuteExport

## 摘要
執行匯出作業的操作。

## 句法

### 執行 (預設) 
```
Invoke-AzCostManagementExecuteExport -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ExecuteViaIdentity
```
Invoke-AzCostManagementExecuteExport -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 說明
執行匯出作業的操作。

## 示例

### 範例1：由 ExportName 和範圍來喚醒呼叫匯出
```powershell
PS C:\> Invoke-AzCostManagementExecuteExport -ExportName 'TestExport' -Scope 'subscriptions/**********'

```

呼叫依 ExportName 及範圍匯出

### 範例2：由 InputObject 來喚醒呼叫匯出
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Invoke-AzCostManagementExecuteExport -InputObject $getExport

```

使用 InputObject 來調用匯出

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

### -ExportName
匯出名稱。

```yaml
Type: System.String
Parameter Sets: Execute
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
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: ExecuteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -範圍
這個參數會從不同的觀點「訂閱」、「ResourceGroup」和「提供服務」定義 costmanagement 的範圍。

```yaml
Type: System.String
Parameter Sets: Execute
Aliases:

Required: True
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

### ICostManagementIdentity （CostManagement）的

## 輸出

### System.object

## 筆記

別名

複雜的參數屬性

若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。 如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。


INPUTOBJECT <ICostManagementIdentity> ：身分識別參數
  - `[AlertId <String>]`：警報 ID
  - `[ExportName <String>]`：匯出名稱。
  - `[ExternalCloudProviderId <String>]`：此專案可以是連結帳戶或 [{externalBillingAccountId}] 的 [{externalSubscriptionId} "，與維度/查詢作業搭配使用的合併帳戶。
  - `[ExternalCloudProviderType <ExternalCloudProviderType?>]`：與維度/查詢作業相關聯的外部雲端提供者類型。 這包含合併帳戶的 [externalSubscriptions] 和 [externalBillingAccounts]。
  - `[Id <String>]`：資源身分識別路徑
  - `[Scope <String>]`：與 [查看] 作業相關聯的範圍。 這包括訂閱範圍的 [訂閱/{subscriptionId}]、[訂閱/{subscriptionId}/resourceGroups/{resourceGroupName} "（針對 resourceGroup 範圍）。提供者/Microsoft. 帳單/billingAccounts/{billingAccountId} ' for 帳單帳戶範圍，" 提供者/Microsoft. 帳單/billingAccounts/{billingAccountId}/部門/{departmentId} "的部門範圍，" 提供者/microsoft. 帳單/billingAccounts/{billingAccountId} "（適用于 EnrollmentAccounts 範圍，" 供應商/Microsoft]）。帳單/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId} ' for BillingProfile 範圍，' 提供者/Microsoft. 帳單/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId} ' 適用于 InvoiceSection 範圍，' 提供者/Microsoft. 管理/managementGroups/{managementGroupId} ' 管理群組範圍、' 提供者/Microsoft. CostManagement/externalBillingAccounts/{externalBillingAccountName}」（適用于外部帳單帳戶範圍和「提供者/CostManagement/externalSubscriptions/{externalSubscriptionName}」）。
  - `[ViewName <String>]`：視圖名稱

## 相關連結

