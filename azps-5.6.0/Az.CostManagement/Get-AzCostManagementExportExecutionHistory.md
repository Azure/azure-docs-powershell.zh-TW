---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/get-azcostmanagementexportexecutionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
ms.openlocfilehash: 602797e32e5d29e3dd4ff2b6ade75ff8055efd0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916635"
---
# <span data-ttu-id="3abfb-101">Get-AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="3abfb-101">Get-AzCostManagementExportExecutionHistory</span></span>

## <span data-ttu-id="3abfb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3abfb-102">SYNOPSIS</span></span>
<span data-ttu-id="3abfb-103">取得已定義範圍和匯出名稱之匯出執行歷程記錄的操作。</span><span class="sxs-lookup"><span data-stu-id="3abfb-103">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="3abfb-104">語法</span><span class="sxs-lookup"><span data-stu-id="3abfb-104">SYNTAX</span></span>

### <span data-ttu-id="3abfb-105">取得 (預設) </span><span class="sxs-lookup"><span data-stu-id="3abfb-105">Get (Default)</span></span>
```
Get-AzCostManagementExportExecutionHistory -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="3abfb-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3abfb-106">GetViaIdentity</span></span>
```
Get-AzCostManagementExportExecutionHistory -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3abfb-107">描述</span><span class="sxs-lookup"><span data-stu-id="3abfb-107">DESCRIPTION</span></span>
<span data-ttu-id="3abfb-108">取得已定義範圍和匯出名稱之匯出執行歷程記錄的操作。</span><span class="sxs-lookup"><span data-stu-id="3abfb-108">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="3abfb-109">例子</span><span class="sxs-lookup"><span data-stu-id="3abfb-109">EXAMPLES</span></span>

### <span data-ttu-id="3abfb-110">範例 1：Get AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="3abfb-110">Example 1: Get AzCostManagementExportExecutionHistory</span></span>
```powershell
PS C:\> Get-AzCostManagementExportExecutionHistory -ExportName 'TestExport' -Scope 'subscriptions/**********'

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
```

<span data-ttu-id="3abfb-111">取得 AzCostManagementExportExecutionHistory By ExportName 和 Scope</span><span class="sxs-lookup"><span data-stu-id="3abfb-111">Get AzCostManagementExportExecutionHistory By ExportName and Scope</span></span>

### <span data-ttu-id="3abfb-112">範例 2：Get AzCostManagementExportExecutionHistory by InputObject</span><span class="sxs-lookup"><span data-stu-id="3abfb-112">Example 2: Get AzCostManagementExportExecutionHistory by InputObject</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Get-AzCostManagementExportExecutionHistory -InputObject $getExport

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/
```

<span data-ttu-id="3abfb-113">取得 AzCostManagementExportExecutionHistory By InputObject</span><span class="sxs-lookup"><span data-stu-id="3abfb-113">Get AzCostManagementExportExecutionHistory By InputObject</span></span>

## <span data-ttu-id="3abfb-114">參數</span><span class="sxs-lookup"><span data-stu-id="3abfb-114">PARAMETERS</span></span>

### <span data-ttu-id="3abfb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3abfb-115">-DefaultProfile</span></span>
<span data-ttu-id="3abfb-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3abfb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3abfb-117">-ExportName</span><span class="sxs-lookup"><span data-stu-id="3abfb-117">-ExportName</span></span>
<span data-ttu-id="3abfb-118">匯出名稱。</span><span class="sxs-lookup"><span data-stu-id="3abfb-118">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3abfb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3abfb-119">-InputObject</span></span>
<span data-ttu-id="3abfb-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3abfb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3abfb-121">-範圍</span><span class="sxs-lookup"><span data-stu-id="3abfb-121">-Scope</span></span>
<span data-ttu-id="3abfb-122">此參數會從不同的觀點定義成本管理的範圍，從"訂閱」、"ResourceGroup"和"提供服務"。</span><span class="sxs-lookup"><span data-stu-id="3abfb-122">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3abfb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3abfb-123">CommonParameters</span></span>
<span data-ttu-id="3abfb-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3abfb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3abfb-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3abfb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3abfb-126">輸入</span><span class="sxs-lookup"><span data-stu-id="3abfb-126">INPUTS</span></span>

### <span data-ttu-id="3abfb-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="3abfb-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="3abfb-128">輸出</span><span class="sxs-lookup"><span data-stu-id="3abfb-128">OUTPUTS</span></span>

### <span data-ttu-id="3abfb-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span><span class="sxs-lookup"><span data-stu-id="3abfb-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span></span>

## <span data-ttu-id="3abfb-130">筆記</span><span class="sxs-lookup"><span data-stu-id="3abfb-130">NOTES</span></span>

<span data-ttu-id="3abfb-131">別名</span><span class="sxs-lookup"><span data-stu-id="3abfb-131">ALIASES</span></span>

<span data-ttu-id="3abfb-132">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="3abfb-132">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3abfb-133">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3abfb-133">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3abfb-134">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="3abfb-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3abfb-135">INPUTOBJECT： <ICostManagementIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="3abfb-135">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3abfb-136">`[AlertId <String>]`：警示識別碼</span><span class="sxs-lookup"><span data-stu-id="3abfb-136">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="3abfb-137">`[ExportName <String>]`：匯出名稱。</span><span class="sxs-lookup"><span data-stu-id="3abfb-137">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="3abfb-138">`[ExternalCloudProviderId <String>]`：這可以是連結帳戶的 '{externalSubscriptionId}'，或用於維度/查詢作業之合併帳戶的 '{externalBillingAccountId}'。</span><span class="sxs-lookup"><span data-stu-id="3abfb-138">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="3abfb-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`：與維度/查詢作業相關聯的外部雲端提供者類型。</span><span class="sxs-lookup"><span data-stu-id="3abfb-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="3abfb-140">這包括連結帳戶的'externalSubscriptions'，以及合併帳戶的'externalBillingAccount'。</span><span class="sxs-lookup"><span data-stu-id="3abfb-140">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="3abfb-141">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="3abfb-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3abfb-142">`[Scope <String>]`：與視圖作業相關聯的範圍。</span><span class="sxs-lookup"><span data-stu-id="3abfb-142">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="3abfb-143">這包括訂閱範圍中的 'subscriptions/{subscriptionId}'，resourceGroup 範圍中的 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope， 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/department/{departmentId}' for Department 範圍， 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount範圍， BillingProfile 範圍中的 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}'， 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}'' for InvoiceSection 範圍， 'providers/Microsoft.Management /managementGroups/{managementGroupId}' for Management Group scope， 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccount}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription 範圍.</span><span class="sxs-lookup"><span data-stu-id="3abfb-143">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="3abfb-144">`[ViewName <String>]`：查看名稱</span><span class="sxs-lookup"><span data-stu-id="3abfb-144">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="3abfb-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="3abfb-145">RELATED LINKS</span></span>

