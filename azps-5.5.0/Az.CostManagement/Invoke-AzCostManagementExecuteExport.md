---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/invoke-azcostmanagementexecuteexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementExecuteExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementExecuteExport.md
ms.openlocfilehash: 752af43a72151296c4c90ecc32923a786c7b4081
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100137362"
---
# <span data-ttu-id="8ac31-101">Invoke-AzCostManagementExecuteExport</span><span class="sxs-lookup"><span data-stu-id="8ac31-101">Invoke-AzCostManagementExecuteExport</span></span>

## <span data-ttu-id="8ac31-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8ac31-102">SYNOPSIS</span></span>
<span data-ttu-id="8ac31-103">執行匯出作業的操作。</span><span class="sxs-lookup"><span data-stu-id="8ac31-103">The operation to execute an export.</span></span>

## <span data-ttu-id="8ac31-104">句法</span><span class="sxs-lookup"><span data-stu-id="8ac31-104">SYNTAX</span></span>

### <span data-ttu-id="8ac31-105">執行 (預設) </span><span class="sxs-lookup"><span data-stu-id="8ac31-105">Execute (Default)</span></span>
```
Invoke-AzCostManagementExecuteExport -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8ac31-106">ExecuteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8ac31-106">ExecuteViaIdentity</span></span>
```
Invoke-AzCostManagementExecuteExport -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8ac31-107">說明</span><span class="sxs-lookup"><span data-stu-id="8ac31-107">DESCRIPTION</span></span>
<span data-ttu-id="8ac31-108">執行匯出作業的操作。</span><span class="sxs-lookup"><span data-stu-id="8ac31-108">The operation to execute an export.</span></span>

## <span data-ttu-id="8ac31-109">示例</span><span class="sxs-lookup"><span data-stu-id="8ac31-109">EXAMPLES</span></span>

### <span data-ttu-id="8ac31-110">範例1：由 ExportName 和範圍來喚醒呼叫匯出</span><span class="sxs-lookup"><span data-stu-id="8ac31-110">Example 1: Invoke Export by ExportName and Scope</span></span>
```powershell
PS C:\> Invoke-AzCostManagementExecuteExport -ExportName 'TestExport' -Scope 'subscriptions/**********'

```

<span data-ttu-id="8ac31-111">呼叫依 ExportName 及範圍匯出</span><span class="sxs-lookup"><span data-stu-id="8ac31-111">Invoke Export by ExportName and Scope</span></span>

### <span data-ttu-id="8ac31-112">範例2：由 InputObject 來喚醒呼叫匯出</span><span class="sxs-lookup"><span data-stu-id="8ac31-112">Example 2: Invoke Export by InputObject</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Invoke-AzCostManagementExecuteExport -InputObject $getExport

```

<span data-ttu-id="8ac31-113">使用 InputObject 來調用匯出</span><span class="sxs-lookup"><span data-stu-id="8ac31-113">Invoke Export by InputObject</span></span>

## <span data-ttu-id="8ac31-114">參數</span><span class="sxs-lookup"><span data-stu-id="8ac31-114">PARAMETERS</span></span>

### <span data-ttu-id="8ac31-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ac31-115">-DefaultProfile</span></span>
<span data-ttu-id="8ac31-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8ac31-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ac31-117">-ExportName</span><span class="sxs-lookup"><span data-stu-id="8ac31-117">-ExportName</span></span>
<span data-ttu-id="8ac31-118">匯出名稱。</span><span class="sxs-lookup"><span data-stu-id="8ac31-118">Export Name.</span></span>

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

### <span data-ttu-id="8ac31-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ac31-119">-InputObject</span></span>
<span data-ttu-id="8ac31-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8ac31-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8ac31-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ac31-121">-PassThru</span></span>
<span data-ttu-id="8ac31-122">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="8ac31-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8ac31-123">-範圍</span><span class="sxs-lookup"><span data-stu-id="8ac31-123">-Scope</span></span>
<span data-ttu-id="8ac31-124">這個參數會從不同的觀點「訂閱」、「ResourceGroup」和「提供服務」定義 costmanagement 的範圍。</span><span class="sxs-lookup"><span data-stu-id="8ac31-124">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="8ac31-125">-確認</span><span class="sxs-lookup"><span data-stu-id="8ac31-125">-Confirm</span></span>
<span data-ttu-id="8ac31-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8ac31-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ac31-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ac31-127">-WhatIf</span></span>
<span data-ttu-id="8ac31-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8ac31-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ac31-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8ac31-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ac31-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ac31-130">CommonParameters</span></span>
<span data-ttu-id="8ac31-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8ac31-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ac31-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8ac31-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ac31-133">輸入</span><span class="sxs-lookup"><span data-stu-id="8ac31-133">INPUTS</span></span>

### <span data-ttu-id="8ac31-134">ICostManagementIdentity （CostManagement）的</span><span class="sxs-lookup"><span data-stu-id="8ac31-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="8ac31-135">輸出</span><span class="sxs-lookup"><span data-stu-id="8ac31-135">OUTPUTS</span></span>

### <span data-ttu-id="8ac31-136">System.object</span><span class="sxs-lookup"><span data-stu-id="8ac31-136">System.Boolean</span></span>

## <span data-ttu-id="8ac31-137">筆記</span><span class="sxs-lookup"><span data-stu-id="8ac31-137">NOTES</span></span>

<span data-ttu-id="8ac31-138">別名</span><span class="sxs-lookup"><span data-stu-id="8ac31-138">ALIASES</span></span>

<span data-ttu-id="8ac31-139">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="8ac31-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8ac31-140">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="8ac31-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8ac31-141">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8ac31-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8ac31-142">INPUTOBJECT <ICostManagementIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="8ac31-142">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8ac31-143">`[AlertId <String>]`：警報 ID</span><span class="sxs-lookup"><span data-stu-id="8ac31-143">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="8ac31-144">`[ExportName <String>]`：匯出名稱。</span><span class="sxs-lookup"><span data-stu-id="8ac31-144">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="8ac31-145">`[ExternalCloudProviderId <String>]`：此專案可以是連結帳戶或 [{externalBillingAccountId}] 的 [{externalSubscriptionId} "，與維度/查詢作業搭配使用的合併帳戶。</span><span class="sxs-lookup"><span data-stu-id="8ac31-145">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="8ac31-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`：與維度/查詢作業相關聯的外部雲端提供者類型。</span><span class="sxs-lookup"><span data-stu-id="8ac31-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="8ac31-147">這包含合併帳戶的 [externalSubscriptions] 和 [externalBillingAccounts]。</span><span class="sxs-lookup"><span data-stu-id="8ac31-147">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="8ac31-148">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="8ac31-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8ac31-149">`[Scope <String>]`：與 [查看] 作業相關聯的範圍。</span><span class="sxs-lookup"><span data-stu-id="8ac31-149">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="8ac31-150">這包括訂閱範圍的 [訂閱/{subscriptionId}]、[訂閱/{subscriptionId}/resourceGroups/{resourceGroupName} "（針對 resourceGroup 範圍）。提供者/Microsoft. 帳單/billingAccounts/{billingAccountId} ' for 帳單帳戶範圍，" 提供者/Microsoft. 帳單/billingAccounts/{billingAccountId}/部門/{departmentId} "的部門範圍，" 提供者/microsoft. 帳單/billingAccounts/{billingAccountId} "（適用于 EnrollmentAccounts 範圍，" 供應商/Microsoft]）。帳單/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId} ' for BillingProfile 範圍，' 提供者/Microsoft. 帳單/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId} ' 適用于 InvoiceSection 範圍，' 提供者/Microsoft. 管理/managementGroups/{managementGroupId} ' 管理群組範圍、' 提供者/Microsoft. CostManagement/externalBillingAccounts/{externalBillingAccountName}」（適用于外部帳單帳戶範圍和「提供者/CostManagement/externalSubscriptions/{externalSubscriptionName}」）。</span><span class="sxs-lookup"><span data-stu-id="8ac31-150">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="8ac31-151">`[ViewName <String>]`：視圖名稱</span><span class="sxs-lookup"><span data-stu-id="8ac31-151">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="8ac31-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="8ac31-152">RELATED LINKS</span></span>

