---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/get-azcostmanagementexportexecutionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
ms.openlocfilehash: 7bb337837f9bd2be532c4eead8d8379b7cf04fe9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277456"
---
# <span data-ttu-id="3f0ac-101">Get-AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="3f0ac-101">Get-AzCostManagementExportExecutionHistory</span></span>

## <span data-ttu-id="3f0ac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3f0ac-102">SYNOPSIS</span></span>
<span data-ttu-id="3f0ac-103">此作業可取得已定義範圍及匯出名稱之匯出的執行歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="3f0ac-103">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="3f0ac-104">句法</span><span class="sxs-lookup"><span data-stu-id="3f0ac-104">SYNTAX</span></span>

### <span data-ttu-id="3f0ac-105">取得 (預設) </span><span class="sxs-lookup"><span data-stu-id="3f0ac-105">Get (Default)</span></span>
```
Get-AzCostManagementExportExecutionHistory -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f0ac-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3f0ac-106">GetViaIdentity</span></span>
```
Get-AzCostManagementExportExecutionHistory -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f0ac-107">說明</span><span class="sxs-lookup"><span data-stu-id="3f0ac-107">DESCRIPTION</span></span>
<span data-ttu-id="3f0ac-108">此作業可取得已定義範圍及匯出名稱之匯出的執行歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="3f0ac-108">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="3f0ac-109">示例</span><span class="sxs-lookup"><span data-stu-id="3f0ac-109">EXAMPLES</span></span>

### <span data-ttu-id="3f0ac-110">範例1：取得 AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="3f0ac-110">Example 1: Get AzCostManagementExportExecutionHistory</span></span>
```powershell
PS C:\> Get-AzCostManagementExportExecutionHistory -ExportName 'TestExport' -Scope 'subscriptions/**********'

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
```

<span data-ttu-id="3f0ac-111">透過 ExportName 和範圍取得 AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="3f0ac-111">Get AzCostManagementExportExecutionHistory By ExportName and Scope</span></span>

### <span data-ttu-id="3f0ac-112">範例2：透過 InputObject 取得 AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="3f0ac-112">Example 2: Get AzCostManagementExportExecutionHistory by InputObject</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Get-AzCostManagementExportExecutionHistory -InputObject $getExport

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/
```

<span data-ttu-id="3f0ac-113">透過 InputObject 取得 AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="3f0ac-113">Get AzCostManagementExportExecutionHistory By InputObject</span></span>

## <span data-ttu-id="3f0ac-114">參數</span><span class="sxs-lookup"><span data-stu-id="3f0ac-114">PARAMETERS</span></span>

### <span data-ttu-id="3f0ac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f0ac-115">-DefaultProfile</span></span>
<span data-ttu-id="3f0ac-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3f0ac-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f0ac-117">-ExportName</span><span class="sxs-lookup"><span data-stu-id="3f0ac-117">-ExportName</span></span>
<span data-ttu-id="3f0ac-118">匯出名稱。</span><span class="sxs-lookup"><span data-stu-id="3f0ac-118">Export Name.</span></span>

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

### <span data-ttu-id="3f0ac-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f0ac-119">-InputObject</span></span>
<span data-ttu-id="3f0ac-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3f0ac-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3f0ac-121">-範圍</span><span class="sxs-lookup"><span data-stu-id="3f0ac-121">-Scope</span></span>
<span data-ttu-id="3f0ac-122">這個參數會從不同的觀點「訂閱」、「ResourceGroup」和「提供服務」定義 costmanagement 的範圍。</span><span class="sxs-lookup"><span data-stu-id="3f0ac-122">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="3f0ac-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f0ac-123">CommonParameters</span></span>
<span data-ttu-id="3f0ac-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3f0ac-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f0ac-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3f0ac-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f0ac-126">輸入</span><span class="sxs-lookup"><span data-stu-id="3f0ac-126">INPUTS</span></span>

### <span data-ttu-id="3f0ac-127">ICostManagementIdentity （CostManagement）的</span><span class="sxs-lookup"><span data-stu-id="3f0ac-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="3f0ac-128">輸出</span><span class="sxs-lookup"><span data-stu-id="3f0ac-128">OUTPUTS</span></span>

### <span data-ttu-id="3f0ac-129">IExportExecution （CostManagement）。 Api20200601。</span><span class="sxs-lookup"><span data-stu-id="3f0ac-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span></span>

## <span data-ttu-id="3f0ac-130">筆記</span><span class="sxs-lookup"><span data-stu-id="3f0ac-130">NOTES</span></span>

<span data-ttu-id="3f0ac-131">別名</span><span class="sxs-lookup"><span data-stu-id="3f0ac-131">ALIASES</span></span>

<span data-ttu-id="3f0ac-132">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="3f0ac-132">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3f0ac-133">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="3f0ac-133">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3f0ac-134">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="3f0ac-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3f0ac-135">INPUTOBJECT <ICostManagementIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="3f0ac-135">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3f0ac-136">`[AlertId <String>]`：警報 ID</span><span class="sxs-lookup"><span data-stu-id="3f0ac-136">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="3f0ac-137">`[ExportName <String>]`：匯出名稱。</span><span class="sxs-lookup"><span data-stu-id="3f0ac-137">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="3f0ac-138">`[ExternalCloudProviderId <String>]`：此專案可以是連結帳戶或 [{externalBillingAccountId}] 的 [{externalSubscriptionId} "，與維度/查詢作業搭配使用的合併帳戶。</span><span class="sxs-lookup"><span data-stu-id="3f0ac-138">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="3f0ac-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`：與維度/查詢作業相關聯的外部雲端提供者類型。</span><span class="sxs-lookup"><span data-stu-id="3f0ac-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="3f0ac-140">這包含合併帳戶的 [externalSubscriptions] 和 [externalBillingAccounts]。</span><span class="sxs-lookup"><span data-stu-id="3f0ac-140">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="3f0ac-141">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="3f0ac-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3f0ac-142">`[Scope <String>]`：與 [查看] 作業相關聯的範圍。</span><span class="sxs-lookup"><span data-stu-id="3f0ac-142">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="3f0ac-143">這包括訂閱範圍的 [訂閱/{subscriptionId}]、[訂閱/{subscriptionId}/resourceGroups/{resourceGroupName} "（針對 resourceGroup 範圍）。提供者/Microsoft. 帳單/billingAccounts/{billingAccountId} ' for 帳單帳戶範圍，" 提供者/Microsoft. 帳單/billingAccounts/{billingAccountId}/部門/{departmentId} "的部門範圍，" 提供者/microsoft. 帳單/billingAccounts/{billingAccountId} "（適用于 EnrollmentAccounts 範圍，" 供應商/Microsoft]）。帳單/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId} ' for BillingProfile 範圍，' 提供者/Microsoft. 帳單/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId} ' 適用于 InvoiceSection 範圍，' 提供者/Microsoft. 管理/managementGroups/{managementGroupId} ' 管理群組範圍、' 提供者/Microsoft. CostManagement/externalBillingAccounts/{externalBillingAccountName}」（適用于外部帳單帳戶範圍和「提供者/CostManagement/externalSubscriptions/{externalSubscriptionName}」）。</span><span class="sxs-lookup"><span data-stu-id="3f0ac-143">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="3f0ac-144">`[ViewName <String>]`：視圖名稱</span><span class="sxs-lookup"><span data-stu-id="3f0ac-144">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="3f0ac-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f0ac-145">RELATED LINKS</span></span>

