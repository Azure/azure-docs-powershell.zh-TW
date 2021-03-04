---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/get-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
ms.openlocfilehash: f318fcf3592c0b865684df57230f73a5f22ce024
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913570"
---
# Get-AzCostManagementExport

## 簡介
以匯出名稱取得已定義範圍匯出的作業。

## 語法

### 清單 (預設) 
```
Get-AzCostManagementExport -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### 獲取
```
Get-AzCostManagementExport -Name <String> -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzCostManagementExport -InputObject <ICostManagementIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## 描述
以匯出名稱取得已定義範圍匯出的作業。

## 例子

### 範例 1：取得所有 AzCostManagementExports by scope
```powershell
PS C:\> Get-AzCostManagementExport -Scope 'subscriptions/**********'

ETag              Name                               Type
----              ----                               ----
"************" TestExport                         Microsoft.CostManagement/exports
"************" TestExport1                        Microsoft.CostManagement/exports
"************" TestExport2                        Microsoft.CostManagement/exports
```

根據範圍取得所有 AzCostManagementExports

### 範例 2：取得 AzCostManagementExport by Name 和 scope
```powershell
PS C:\> Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'

ETag              Name       Type
----              ----       ----
"************" TestExport Microsoft.CostManagement/exports
```

根據名稱和範圍取得 AzCostManagementExport

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

### -展開
可用於展開匯出中的屬性。
目前僅支援 'runHistory'，並會針對匯出的最後 10 個執行程式，返回相關資訊。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
匯出名稱。

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -範圍
此參數會從不同的觀點定義成本管理的範圍，從"訂閱」、"ResourceGroup"和"提供服務"。

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### Microsoft.Azure.PowerShell.Cmdlets.CostManagement.models.ICostManagementIdentity

## 輸出

### Microsoft.Azure.PowerShell.Cmdlets.CostManagement.models.Api20200601.IExport

## 筆記

別名

複雜的參數屬性

若要建立下列描述的參數，請建構包含適當屬性的雜湊表。 有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。


INPUTOBJECT： <ICostManagementIdentity> 身分識別參數
  - `[AlertId <String>]`：警示識別碼
  - `[ExportName <String>]`：匯出名稱。
  - `[ExternalCloudProviderId <String>]`：這可以是連結帳戶的 '{externalSubscriptionId}'，或用於維度/查詢作業之合併帳戶的 '{externalBillingAccountId}'。
  - `[ExternalCloudProviderType <ExternalCloudProviderType?>]`：與維度/查詢作業相關聯的外部雲端提供者類型。 這包括連結帳戶的'externalSubscriptions'，以及合併帳戶的'externalBillingAccount'。
  - `[Id <String>]`：資源識別路徑
  - `[Scope <String>]`：與視圖作業相關聯的範圍。 這包括訂閱範圍中的 'subscriptions/{subscriptionId}'，resourceGroup 範圍中的 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope， 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/department/{departmentId}' for Department 範圍， 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount範圍， BillingProfile 範圍中的 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}'， 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}'' for InvoiceSection 範圍， 'providers/Microsoft.Management /managementGroups/{managementGroupId}' for Management Group scope， 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccount}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription 範圍.
  - `[ViewName <String>]`：查看名稱

## 相關連結

