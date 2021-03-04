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
# <span data-ttu-id="7075e-101">Get-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="7075e-101">Get-AzCostManagementExport</span></span>

## <span data-ttu-id="7075e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7075e-102">SYNOPSIS</span></span>
<span data-ttu-id="7075e-103">以匯出名稱取得已定義範圍匯出的作業。</span><span class="sxs-lookup"><span data-stu-id="7075e-103">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="7075e-104">語法</span><span class="sxs-lookup"><span data-stu-id="7075e-104">SYNTAX</span></span>

### <span data-ttu-id="7075e-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="7075e-105">List (Default)</span></span>
```
Get-AzCostManagementExport -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="7075e-106">獲取</span><span class="sxs-lookup"><span data-stu-id="7075e-106">Get</span></span>
```
Get-AzCostManagementExport -Name <String> -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="7075e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7075e-107">GetViaIdentity</span></span>
```
Get-AzCostManagementExport -InputObject <ICostManagementIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7075e-108">描述</span><span class="sxs-lookup"><span data-stu-id="7075e-108">DESCRIPTION</span></span>
<span data-ttu-id="7075e-109">以匯出名稱取得已定義範圍匯出的作業。</span><span class="sxs-lookup"><span data-stu-id="7075e-109">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="7075e-110">例子</span><span class="sxs-lookup"><span data-stu-id="7075e-110">EXAMPLES</span></span>

### <span data-ttu-id="7075e-111">範例 1：取得所有 AzCostManagementExports by scope</span><span class="sxs-lookup"><span data-stu-id="7075e-111">Example 1: Get all AzCostManagementExports by scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Scope 'subscriptions/**********'

ETag              Name                               Type
----              ----                               ----
"************" TestExport                         Microsoft.CostManagement/exports
"************" TestExport1                        Microsoft.CostManagement/exports
"************" TestExport2                        Microsoft.CostManagement/exports
```

<span data-ttu-id="7075e-112">根據範圍取得所有 AzCostManagementExports</span><span class="sxs-lookup"><span data-stu-id="7075e-112">Get all AzCostManagementExports by Scope</span></span>

### <span data-ttu-id="7075e-113">範例 2：取得 AzCostManagementExport by Name 和 scope</span><span class="sxs-lookup"><span data-stu-id="7075e-113">Example 2: Get AzCostManagementExport by Name and scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'

ETag              Name       Type
----              ----       ----
"************" TestExport Microsoft.CostManagement/exports
```

<span data-ttu-id="7075e-114">根據名稱和範圍取得 AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="7075e-114">Get AzCostManagementExport by Name and scope</span></span>

## <span data-ttu-id="7075e-115">參數</span><span class="sxs-lookup"><span data-stu-id="7075e-115">PARAMETERS</span></span>

### <span data-ttu-id="7075e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7075e-116">-DefaultProfile</span></span>
<span data-ttu-id="7075e-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7075e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7075e-118">-展開</span><span class="sxs-lookup"><span data-stu-id="7075e-118">-Expand</span></span>
<span data-ttu-id="7075e-119">可用於展開匯出中的屬性。</span><span class="sxs-lookup"><span data-stu-id="7075e-119">May be used to expand the properties within an export.</span></span>
<span data-ttu-id="7075e-120">目前僅支援 'runHistory'，並會針對匯出的最後 10 個執行程式，返回相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7075e-120">Currently only 'runHistory' is supported and will return information for the last 10 executions of the export.</span></span>

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

### <span data-ttu-id="7075e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7075e-121">-InputObject</span></span>
<span data-ttu-id="7075e-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="7075e-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7075e-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="7075e-123">-Name</span></span>
<span data-ttu-id="7075e-124">匯出名稱。</span><span class="sxs-lookup"><span data-stu-id="7075e-124">Export Name.</span></span>

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

### <span data-ttu-id="7075e-125">-範圍</span><span class="sxs-lookup"><span data-stu-id="7075e-125">-Scope</span></span>
<span data-ttu-id="7075e-126">此參數會從不同的觀點定義成本管理的範圍，從"訂閱」、"ResourceGroup"和"提供服務"。</span><span class="sxs-lookup"><span data-stu-id="7075e-126">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="7075e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7075e-127">CommonParameters</span></span>
<span data-ttu-id="7075e-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7075e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7075e-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7075e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7075e-130">輸入</span><span class="sxs-lookup"><span data-stu-id="7075e-130">INPUTS</span></span>

### <span data-ttu-id="7075e-131">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="7075e-131">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="7075e-132">輸出</span><span class="sxs-lookup"><span data-stu-id="7075e-132">OUTPUTS</span></span>

### <span data-ttu-id="7075e-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="7075e-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="7075e-134">筆記</span><span class="sxs-lookup"><span data-stu-id="7075e-134">NOTES</span></span>

<span data-ttu-id="7075e-135">別名</span><span class="sxs-lookup"><span data-stu-id="7075e-135">ALIASES</span></span>

<span data-ttu-id="7075e-136">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="7075e-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7075e-137">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="7075e-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7075e-138">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="7075e-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7075e-139">INPUTOBJECT： <ICostManagementIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="7075e-139">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7075e-140">`[AlertId <String>]`：警示識別碼</span><span class="sxs-lookup"><span data-stu-id="7075e-140">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="7075e-141">`[ExportName <String>]`：匯出名稱。</span><span class="sxs-lookup"><span data-stu-id="7075e-141">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="7075e-142">`[ExternalCloudProviderId <String>]`：這可以是連結帳戶的 '{externalSubscriptionId}'，或用於維度/查詢作業之合併帳戶的 '{externalBillingAccountId}'。</span><span class="sxs-lookup"><span data-stu-id="7075e-142">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="7075e-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`：與維度/查詢作業相關聯的外部雲端提供者類型。</span><span class="sxs-lookup"><span data-stu-id="7075e-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="7075e-144">這包括連結帳戶的'externalSubscriptions'，以及合併帳戶的'externalBillingAccount'。</span><span class="sxs-lookup"><span data-stu-id="7075e-144">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="7075e-145">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="7075e-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7075e-146">`[Scope <String>]`：與視圖作業相關聯的範圍。</span><span class="sxs-lookup"><span data-stu-id="7075e-146">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="7075e-147">這包括訂閱範圍中的 'subscriptions/{subscriptionId}'，resourceGroup 範圍中的 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope， 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/department/{departmentId}' for Department 範圍， 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount範圍， BillingProfile 範圍中的 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}'， 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}'' for InvoiceSection 範圍， 'providers/Microsoft.Management /managementGroups/{managementGroupId}' for Management Group scope， 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccount}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription 範圍.</span><span class="sxs-lookup"><span data-stu-id="7075e-147">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="7075e-148">`[ViewName <String>]`：查看名稱</span><span class="sxs-lookup"><span data-stu-id="7075e-148">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="7075e-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="7075e-149">RELATED LINKS</span></span>

