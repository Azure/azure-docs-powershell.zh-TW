---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/get-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
ms.openlocfilehash: 269a58e57510f6b0945218645ec079b21b606e44
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277460"
---
# <span data-ttu-id="4d310-101">Get-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="4d310-101">Get-AzCostManagementExport</span></span>

## <span data-ttu-id="4d310-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4d310-102">SYNOPSIS</span></span>
<span data-ttu-id="4d310-103">此作業可透過匯出名稱取得已定義範圍的匯出。</span><span class="sxs-lookup"><span data-stu-id="4d310-103">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="4d310-104">句法</span><span class="sxs-lookup"><span data-stu-id="4d310-104">SYNTAX</span></span>

### <span data-ttu-id="4d310-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="4d310-105">List (Default)</span></span>
```
Get-AzCostManagementExport -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="4d310-106">獲取</span><span class="sxs-lookup"><span data-stu-id="4d310-106">Get</span></span>
```
Get-AzCostManagementExport -Name <String> -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="4d310-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4d310-107">GetViaIdentity</span></span>
```
Get-AzCostManagementExport -InputObject <ICostManagementIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4d310-108">說明</span><span class="sxs-lookup"><span data-stu-id="4d310-108">DESCRIPTION</span></span>
<span data-ttu-id="4d310-109">此作業可透過匯出名稱取得已定義範圍的匯出。</span><span class="sxs-lookup"><span data-stu-id="4d310-109">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="4d310-110">示例</span><span class="sxs-lookup"><span data-stu-id="4d310-110">EXAMPLES</span></span>

### <span data-ttu-id="4d310-111">範例1：依範圍取得所有 AzCostManagementExports</span><span class="sxs-lookup"><span data-stu-id="4d310-111">Example 1: Get all AzCostManagementExports by scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Scope 'subscriptions/**********'

ETag              Name                               Type
----              ----                               ----
"************" TestExport                         Microsoft.CostManagement/exports
"************" TestExport1                        Microsoft.CostManagement/exports
"************" TestExport2                        Microsoft.CostManagement/exports
```

<span data-ttu-id="4d310-112">依範圍取得所有 AzCostManagementExports</span><span class="sxs-lookup"><span data-stu-id="4d310-112">Get all AzCostManagementExports by Scope</span></span>

### <span data-ttu-id="4d310-113">範例2：依名稱和範圍取得 AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="4d310-113">Example 2: Get AzCostManagementExport by Name and scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'

ETag              Name       Type
----              ----       ----
"************" TestExport Microsoft.CostManagement/exports
```

<span data-ttu-id="4d310-114">依名稱和範圍取得 AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="4d310-114">Get AzCostManagementExport by Name and scope</span></span>

## <span data-ttu-id="4d310-115">參數</span><span class="sxs-lookup"><span data-stu-id="4d310-115">PARAMETERS</span></span>

### <span data-ttu-id="4d310-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d310-116">-DefaultProfile</span></span>
<span data-ttu-id="4d310-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4d310-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d310-118">-展開</span><span class="sxs-lookup"><span data-stu-id="4d310-118">-Expand</span></span>
<span data-ttu-id="4d310-119">可用於展開匯出中的屬性。</span><span class="sxs-lookup"><span data-stu-id="4d310-119">May be used to expand the properties within an export.</span></span>
<span data-ttu-id="4d310-120">目前僅支援 ' runHistory」，且會傳回匯出最後10次執行的資訊。</span><span class="sxs-lookup"><span data-stu-id="4d310-120">Currently only 'runHistory' is supported and will return information for the last 10 executions of the export.</span></span>

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

### <span data-ttu-id="4d310-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d310-121">-InputObject</span></span>
<span data-ttu-id="4d310-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4d310-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4d310-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="4d310-123">-Name</span></span>
<span data-ttu-id="4d310-124">匯出名稱。</span><span class="sxs-lookup"><span data-stu-id="4d310-124">Export Name.</span></span>

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

### <span data-ttu-id="4d310-125">-範圍</span><span class="sxs-lookup"><span data-stu-id="4d310-125">-Scope</span></span>
<span data-ttu-id="4d310-126">這個參數會從不同的觀點「訂閱」、「ResourceGroup」和「提供服務」定義 costmanagement 的範圍。</span><span class="sxs-lookup"><span data-stu-id="4d310-126">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="4d310-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d310-127">CommonParameters</span></span>
<span data-ttu-id="4d310-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4d310-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d310-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4d310-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d310-130">輸入</span><span class="sxs-lookup"><span data-stu-id="4d310-130">INPUTS</span></span>

### <span data-ttu-id="4d310-131">ICostManagementIdentity （CostManagement）的</span><span class="sxs-lookup"><span data-stu-id="4d310-131">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="4d310-132">輸出</span><span class="sxs-lookup"><span data-stu-id="4d310-132">OUTPUTS</span></span>

### <span data-ttu-id="4d310-133">IExport （CostManagement）。 Api20200601。</span><span class="sxs-lookup"><span data-stu-id="4d310-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="4d310-134">筆記</span><span class="sxs-lookup"><span data-stu-id="4d310-134">NOTES</span></span>

<span data-ttu-id="4d310-135">別名</span><span class="sxs-lookup"><span data-stu-id="4d310-135">ALIASES</span></span>

<span data-ttu-id="4d310-136">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="4d310-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4d310-137">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="4d310-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4d310-138">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="4d310-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4d310-139">INPUTOBJECT <ICostManagementIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="4d310-139">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4d310-140">`[AlertId <String>]`：警報 ID</span><span class="sxs-lookup"><span data-stu-id="4d310-140">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="4d310-141">`[ExportName <String>]`：匯出名稱。</span><span class="sxs-lookup"><span data-stu-id="4d310-141">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="4d310-142">`[ExternalCloudProviderId <String>]`：此專案可以是連結帳戶或 [{externalBillingAccountId}] 的 [{externalSubscriptionId} "，與維度/查詢作業搭配使用的合併帳戶。</span><span class="sxs-lookup"><span data-stu-id="4d310-142">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="4d310-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`：與維度/查詢作業相關聯的外部雲端提供者類型。</span><span class="sxs-lookup"><span data-stu-id="4d310-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="4d310-144">這包含合併帳戶的 [externalSubscriptions] 和 [externalBillingAccounts]。</span><span class="sxs-lookup"><span data-stu-id="4d310-144">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="4d310-145">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="4d310-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4d310-146">`[Scope <String>]`：與 [查看] 作業相關聯的範圍。</span><span class="sxs-lookup"><span data-stu-id="4d310-146">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="4d310-147">這包括訂閱範圍的 [訂閱/{subscriptionId}]、[訂閱/{subscriptionId}/resourceGroups/{resourceGroupName} "（針對 resourceGroup 範圍）。提供者/Microsoft. 帳單/billingAccounts/{billingAccountId} ' for 帳單帳戶範圍，" 提供者/Microsoft. 帳單/billingAccounts/{billingAccountId}/部門/{departmentId} "的部門範圍，" 提供者/microsoft. 帳單/billingAccounts/{billingAccountId} "（適用于 EnrollmentAccounts 範圍，" 供應商/Microsoft]）。帳單/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId} ' for BillingProfile 範圍，' 提供者/Microsoft. 帳單/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId} ' 適用于 InvoiceSection 範圍，' 提供者/Microsoft. 管理/managementGroups/{managementGroupId} ' 管理群組範圍、' 提供者/Microsoft. CostManagement/externalBillingAccounts/{externalBillingAccountName}」（適用于外部帳單帳戶範圍和「提供者/CostManagement/externalSubscriptions/{externalSubscriptionName}」）。</span><span class="sxs-lookup"><span data-stu-id="4d310-147">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="4d310-148">`[ViewName <String>]`：視圖名稱</span><span class="sxs-lookup"><span data-stu-id="4d310-148">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="4d310-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="4d310-149">RELATED LINKS</span></span>

