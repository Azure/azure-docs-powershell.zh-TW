---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/remove-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
ms.openlocfilehash: 75c1f01730d4dfe3e9769a430f874887fd2d2090
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277432"
---
# <span data-ttu-id="5a578-101">Remove-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="5a578-101">Remove-AzCostManagementExport</span></span>

## <span data-ttu-id="5a578-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5a578-102">SYNOPSIS</span></span>
<span data-ttu-id="5a578-103">刪除匯出的操作。</span><span class="sxs-lookup"><span data-stu-id="5a578-103">The operation to delete a export.</span></span>

## <span data-ttu-id="5a578-104">句法</span><span class="sxs-lookup"><span data-stu-id="5a578-104">SYNTAX</span></span>

### <span data-ttu-id="5a578-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="5a578-105">Delete (Default)</span></span>
```
Remove-AzCostManagementExport -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5a578-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5a578-106">DeleteViaIdentity</span></span>
```
Remove-AzCostManagementExport -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5a578-107">說明</span><span class="sxs-lookup"><span data-stu-id="5a578-107">DESCRIPTION</span></span>
<span data-ttu-id="5a578-108">刪除匯出的操作。</span><span class="sxs-lookup"><span data-stu-id="5a578-108">The operation to delete a export.</span></span>

## <span data-ttu-id="5a578-109">示例</span><span class="sxs-lookup"><span data-stu-id="5a578-109">EXAMPLES</span></span>

### <span data-ttu-id="5a578-110">範例1：依範圍和名稱刪除 AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="5a578-110">Example 1: Delete the AzCostManagementExport by Scope and Name</span></span>
```powershell
PS C:\> Remove-AzCostManagementExport -Scope 'subscriptions/********' -name 'TestExportDatasetAggregationInfoYouri'


```

<span data-ttu-id="5a578-111">依範圍和 ExportName 刪除 AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="5a578-111">Delete the AzCostManagementExport By Scope and ExportName</span></span>

### <span data-ttu-id="5a578-112">範例2：透過匯出物件刪除 AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="5a578-112">Example 2: Delete the AzCostManagementExport by Export Object</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Scope 'subscriptions/*********' -name 'TestExportDatasetAggregationYouori'
Remove-AzCostManagementExport -InputObject $getExport


```

<span data-ttu-id="5a578-113">刪除 AzCostManagementExport By InputObject</span><span class="sxs-lookup"><span data-stu-id="5a578-113">Delete the AzCostManagementExport By InputObject</span></span>

## <span data-ttu-id="5a578-114">參數</span><span class="sxs-lookup"><span data-stu-id="5a578-114">PARAMETERS</span></span>

### <span data-ttu-id="5a578-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a578-115">-DefaultProfile</span></span>
<span data-ttu-id="5a578-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5a578-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a578-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a578-117">-InputObject</span></span>
<span data-ttu-id="5a578-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5a578-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5a578-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="5a578-119">-Name</span></span>
<span data-ttu-id="5a578-120">匯出名稱。</span><span class="sxs-lookup"><span data-stu-id="5a578-120">Export Name.</span></span>

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

### <span data-ttu-id="5a578-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a578-121">-PassThru</span></span>
<span data-ttu-id="5a578-122">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="5a578-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5a578-123">-範圍</span><span class="sxs-lookup"><span data-stu-id="5a578-123">-Scope</span></span>
<span data-ttu-id="5a578-124">這個參數會從不同的觀點「訂閱」、「ResourceGroup」和「提供服務」定義 costmanagement 的範圍。</span><span class="sxs-lookup"><span data-stu-id="5a578-124">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="5a578-125">-確認</span><span class="sxs-lookup"><span data-stu-id="5a578-125">-Confirm</span></span>
<span data-ttu-id="5a578-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5a578-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a578-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a578-127">-WhatIf</span></span>
<span data-ttu-id="5a578-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5a578-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a578-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5a578-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a578-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a578-130">CommonParameters</span></span>
<span data-ttu-id="5a578-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5a578-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a578-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5a578-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a578-133">輸入</span><span class="sxs-lookup"><span data-stu-id="5a578-133">INPUTS</span></span>

### <span data-ttu-id="5a578-134">ICostManagementIdentity （CostManagement）的</span><span class="sxs-lookup"><span data-stu-id="5a578-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="5a578-135">輸出</span><span class="sxs-lookup"><span data-stu-id="5a578-135">OUTPUTS</span></span>

### <span data-ttu-id="5a578-136">System.object</span><span class="sxs-lookup"><span data-stu-id="5a578-136">System.Boolean</span></span>

## <span data-ttu-id="5a578-137">筆記</span><span class="sxs-lookup"><span data-stu-id="5a578-137">NOTES</span></span>

<span data-ttu-id="5a578-138">別名</span><span class="sxs-lookup"><span data-stu-id="5a578-138">ALIASES</span></span>

<span data-ttu-id="5a578-139">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="5a578-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5a578-140">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="5a578-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5a578-141">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="5a578-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5a578-142">INPUTOBJECT <ICostManagementIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="5a578-142">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5a578-143">`[AlertId <String>]`：警報 ID</span><span class="sxs-lookup"><span data-stu-id="5a578-143">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="5a578-144">`[ExportName <String>]`：匯出名稱。</span><span class="sxs-lookup"><span data-stu-id="5a578-144">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="5a578-145">`[ExternalCloudProviderId <String>]`：此專案可以是連結帳戶或 [{externalBillingAccountId}] 的 [{externalSubscriptionId} "，與維度/查詢作業搭配使用的合併帳戶。</span><span class="sxs-lookup"><span data-stu-id="5a578-145">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="5a578-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`：與維度/查詢作業相關聯的外部雲端提供者類型。</span><span class="sxs-lookup"><span data-stu-id="5a578-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="5a578-147">這包含合併帳戶的 [externalSubscriptions] 和 [externalBillingAccounts]。</span><span class="sxs-lookup"><span data-stu-id="5a578-147">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="5a578-148">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="5a578-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5a578-149">`[Scope <String>]`：與 [查看] 作業相關聯的範圍。</span><span class="sxs-lookup"><span data-stu-id="5a578-149">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="5a578-150">這包括訂閱範圍的 [訂閱/{subscriptionId}]、[訂閱/{subscriptionId}/resourceGroups/{resourceGroupName} "（針對 resourceGroup 範圍）。提供者/Microsoft. 帳單/billingAccounts/{billingAccountId} ' for 帳單帳戶範圍，" 提供者/Microsoft. 帳單/billingAccounts/{billingAccountId}/部門/{departmentId} "的部門範圍，" 提供者/microsoft. 帳單/billingAccounts/{billingAccountId} "（適用于 EnrollmentAccounts 範圍，" 供應商/Microsoft]）。帳單/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId} ' for BillingProfile 範圍，' 提供者/Microsoft. 帳單/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId} ' 適用于 InvoiceSection 範圍，' 提供者/Microsoft. 管理/managementGroups/{managementGroupId} ' 管理群組範圍、' 提供者/Microsoft. CostManagement/externalBillingAccounts/{externalBillingAccountName}」（適用于外部帳單帳戶範圍和「提供者/CostManagement/externalSubscriptions/{externalSubscriptionName}」）。</span><span class="sxs-lookup"><span data-stu-id="5a578-150">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="5a578-151">`[ViewName <String>]`：視圖名稱</span><span class="sxs-lookup"><span data-stu-id="5a578-151">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="5a578-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a578-152">RELATED LINKS</span></span>

