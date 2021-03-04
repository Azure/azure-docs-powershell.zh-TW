---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/remove-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
ms.openlocfilehash: e3c464ee8a2ae038a9e6d8d7578c3e4862c16460
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904525"
---
# <span data-ttu-id="6f559-101">Remove-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="6f559-101">Remove-AzCostManagementExport</span></span>

## <span data-ttu-id="6f559-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6f559-102">SYNOPSIS</span></span>
<span data-ttu-id="6f559-103">刪除匯出的作業。</span><span class="sxs-lookup"><span data-stu-id="6f559-103">The operation to delete a export.</span></span>

## <span data-ttu-id="6f559-104">語法</span><span class="sxs-lookup"><span data-stu-id="6f559-104">SYNTAX</span></span>

### <span data-ttu-id="6f559-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="6f559-105">Delete (Default)</span></span>
```
Remove-AzCostManagementExport -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6f559-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6f559-106">DeleteViaIdentity</span></span>
```
Remove-AzCostManagementExport -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6f559-107">描述</span><span class="sxs-lookup"><span data-stu-id="6f559-107">DESCRIPTION</span></span>
<span data-ttu-id="6f559-108">刪除匯出的作業。</span><span class="sxs-lookup"><span data-stu-id="6f559-108">The operation to delete a export.</span></span>

## <span data-ttu-id="6f559-109">例子</span><span class="sxs-lookup"><span data-stu-id="6f559-109">EXAMPLES</span></span>

### <span data-ttu-id="6f559-110">範例 1：刪除 AzCostManagementExport by Scope 和 Name</span><span class="sxs-lookup"><span data-stu-id="6f559-110">Example 1: Delete the AzCostManagementExport by Scope and Name</span></span>
```powershell
PS C:\> Remove-AzCostManagementExport -Scope 'subscriptions/********' -name 'TestExportDatasetAggregationInfoYouri'


```

<span data-ttu-id="6f559-111">刪除 AzCostManagementExport By Scope 和 ExportName</span><span class="sxs-lookup"><span data-stu-id="6f559-111">Delete the AzCostManagementExport By Scope and ExportName</span></span>

### <span data-ttu-id="6f559-112">範例 2：刪除 AzCostManagementExport by Export Object</span><span class="sxs-lookup"><span data-stu-id="6f559-112">Example 2: Delete the AzCostManagementExport by Export Object</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Scope 'subscriptions/*********' -name 'TestExportDatasetAggregationYouori'
Remove-AzCostManagementExport -InputObject $getExport


```

<span data-ttu-id="6f559-113">刪除 AzCostManagementExport By InputObject</span><span class="sxs-lookup"><span data-stu-id="6f559-113">Delete the AzCostManagementExport By InputObject</span></span>

## <span data-ttu-id="6f559-114">參數</span><span class="sxs-lookup"><span data-stu-id="6f559-114">PARAMETERS</span></span>

### <span data-ttu-id="6f559-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f559-115">-DefaultProfile</span></span>
<span data-ttu-id="6f559-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f559-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f559-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f559-117">-InputObject</span></span>
<span data-ttu-id="6f559-118">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6f559-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f559-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="6f559-119">-Name</span></span>
<span data-ttu-id="6f559-120">匯出名稱。</span><span class="sxs-lookup"><span data-stu-id="6f559-120">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f559-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f559-121">-PassThru</span></span>
<span data-ttu-id="6f559-122">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="6f559-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6f559-123">-範圍</span><span class="sxs-lookup"><span data-stu-id="6f559-123">-Scope</span></span>
<span data-ttu-id="6f559-124">此參數會從不同的觀點定義成本管理的範圍，從"訂閱」、"ResourceGroup"和"提供服務"。</span><span class="sxs-lookup"><span data-stu-id="6f559-124">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="6f559-125">-確認</span><span class="sxs-lookup"><span data-stu-id="6f559-125">-Confirm</span></span>
<span data-ttu-id="6f559-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6f559-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f559-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f559-127">-WhatIf</span></span>
<span data-ttu-id="6f559-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6f559-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f559-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f559-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f559-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f559-130">CommonParameters</span></span>
<span data-ttu-id="6f559-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6f559-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f559-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f559-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f559-133">輸入</span><span class="sxs-lookup"><span data-stu-id="6f559-133">INPUTS</span></span>

### <span data-ttu-id="6f559-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="6f559-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="6f559-135">輸出</span><span class="sxs-lookup"><span data-stu-id="6f559-135">OUTPUTS</span></span>

### <span data-ttu-id="6f559-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6f559-136">System.Boolean</span></span>

## <span data-ttu-id="6f559-137">筆記</span><span class="sxs-lookup"><span data-stu-id="6f559-137">NOTES</span></span>

<span data-ttu-id="6f559-138">別名</span><span class="sxs-lookup"><span data-stu-id="6f559-138">ALIASES</span></span>

<span data-ttu-id="6f559-139">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="6f559-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6f559-140">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6f559-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6f559-141">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="6f559-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6f559-142">INPUTOBJECT： <ICostManagementIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="6f559-142">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6f559-143">`[AlertId <String>]`：警示識別碼</span><span class="sxs-lookup"><span data-stu-id="6f559-143">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="6f559-144">`[ExportName <String>]`：匯出名稱。</span><span class="sxs-lookup"><span data-stu-id="6f559-144">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="6f559-145">`[ExternalCloudProviderId <String>]`：這可以是連結帳戶的 '{externalSubscriptionId}'，或用於維度/查詢作業之合併帳戶的 '{externalBillingAccountId}'。</span><span class="sxs-lookup"><span data-stu-id="6f559-145">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="6f559-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`：與維度/查詢作業相關聯的外部雲端提供者類型。</span><span class="sxs-lookup"><span data-stu-id="6f559-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="6f559-147">這包括連結帳戶的'externalSubscriptions'，以及合併帳戶的'externalBillingAccount'。</span><span class="sxs-lookup"><span data-stu-id="6f559-147">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="6f559-148">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="6f559-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6f559-149">`[Scope <String>]`：與視圖作業相關聯的範圍。</span><span class="sxs-lookup"><span data-stu-id="6f559-149">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="6f559-150">這包括訂閱範圍中的 'subscriptions/{subscriptionId}'，resourceGroup 範圍中的 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope， 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/department/{departmentId}' for Department 範圍， 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount範圍， BillingProfile 範圍中的 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}'， 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}'' for InvoiceSection 範圍， 'providers/Microsoft.Management /managementGroups/{managementGroupId}' for Management Group scope， 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccount}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription 範圍.</span><span class="sxs-lookup"><span data-stu-id="6f559-150">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="6f559-151">`[ViewName <String>]`：查看名稱</span><span class="sxs-lookup"><span data-stu-id="6f559-151">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="6f559-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f559-152">RELATED LINKS</span></span>

