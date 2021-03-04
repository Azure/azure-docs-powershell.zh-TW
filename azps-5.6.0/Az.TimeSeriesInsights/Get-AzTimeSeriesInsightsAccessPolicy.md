---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: 20a9abc5cfc2ad2cc35bbedcf976daac286abb92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907021"
---
# <span data-ttu-id="48cf1-101">Get-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="48cf1-101">Get-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="48cf1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="48cf1-102">SYNOPSIS</span></span>
<span data-ttu-id="48cf1-103">取得指定環境中具有指定名稱的存取策略。</span><span class="sxs-lookup"><span data-stu-id="48cf1-103">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="48cf1-104">語法</span><span class="sxs-lookup"><span data-stu-id="48cf1-104">SYNTAX</span></span>

### <span data-ttu-id="48cf1-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="48cf1-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="48cf1-106">獲取</span><span class="sxs-lookup"><span data-stu-id="48cf1-106">Get</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="48cf1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="48cf1-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="48cf1-108">描述</span><span class="sxs-lookup"><span data-stu-id="48cf1-108">DESCRIPTION</span></span>
<span data-ttu-id="48cf1-109">取得指定環境中具有指定名稱的存取策略。</span><span class="sxs-lookup"><span data-stu-id="48cf1-109">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="48cf1-110">例子</span><span class="sxs-lookup"><span data-stu-id="48cf1-110">EXAMPLES</span></span>

### <span data-ttu-id="48cf1-111">範例 1：列出指定環境中的所有存取策略</span><span class="sxs-lookup"><span data-stu-id="48cf1-111">Example 1: List all access policies under a specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
policy002 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="48cf1-112">此命令會列出指定環境中的所有存取策略。</span><span class="sxs-lookup"><span data-stu-id="48cf1-112">This command lists all access policies under a specified environment.</span></span>

### <span data-ttu-id="48cf1-113">範例 2：根據名稱取得指定的存取策略</span><span class="sxs-lookup"><span data-stu-id="48cf1-113">Example 2: Get a specified access policy by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="48cf1-114">此命令會取得指定的存取策略。</span><span class="sxs-lookup"><span data-stu-id="48cf1-114">This command gets a specified access policy.</span></span>

### <span data-ttu-id="48cf1-115">範例 3：根據物件取得指定的存取策略</span><span class="sxs-lookup"><span data-stu-id="48cf1-115">Example 3: Get a specified access policy by object</span></span>
```powershell
PS C:\>$ap = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsi-envv8u56x -ResourceGroupName tsi-test-i01k5l -Name tsi-apilgj5y 
PS C:\>Get-AzTimeSeriesInsightsAccessPolicy -InputObject $ap

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="48cf1-116">此命令會取得指定的存取策略。</span><span class="sxs-lookup"><span data-stu-id="48cf1-116">This command gets a specified access policy.</span></span>

## <span data-ttu-id="48cf1-117">參數</span><span class="sxs-lookup"><span data-stu-id="48cf1-117">PARAMETERS</span></span>

### <span data-ttu-id="48cf1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48cf1-118">-DefaultProfile</span></span>
<span data-ttu-id="48cf1-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="48cf1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48cf1-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="48cf1-120">-EnvironmentName</span></span>
<span data-ttu-id="48cf1-121">與指定資源群組相關聯的時間序列深入資訊環境名稱。</span><span class="sxs-lookup"><span data-stu-id="48cf1-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="48cf1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48cf1-122">-InputObject</span></span>
<span data-ttu-id="48cf1-123">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="48cf1-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48cf1-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="48cf1-124">-Name</span></span>
<span data-ttu-id="48cf1-125">與指定環境相關聯的時間系列深入資訊存取策略名稱。</span><span class="sxs-lookup"><span data-stu-id="48cf1-125">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48cf1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48cf1-126">-ResourceGroupName</span></span>
<span data-ttu-id="48cf1-127">Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="48cf1-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="48cf1-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="48cf1-128">-SubscriptionId</span></span>
<span data-ttu-id="48cf1-129">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="48cf1-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48cf1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48cf1-130">CommonParameters</span></span>
<span data-ttu-id="48cf1-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="48cf1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48cf1-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48cf1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48cf1-133">輸入</span><span class="sxs-lookup"><span data-stu-id="48cf1-133">INPUTS</span></span>

### <span data-ttu-id="48cf1-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="48cf1-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="48cf1-135">輸出</span><span class="sxs-lookup"><span data-stu-id="48cf1-135">OUTPUTS</span></span>

### <span data-ttu-id="48cf1-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="48cf1-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="48cf1-137">筆記</span><span class="sxs-lookup"><span data-stu-id="48cf1-137">NOTES</span></span>

<span data-ttu-id="48cf1-138">別名</span><span class="sxs-lookup"><span data-stu-id="48cf1-138">ALIASES</span></span>

<span data-ttu-id="48cf1-139">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="48cf1-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="48cf1-140">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="48cf1-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="48cf1-141">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="48cf1-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="48cf1-142">INPUTOBJECT： <ITimeSeriesInsightsIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="48cf1-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="48cf1-143">`[AccessPolicyName <String>]`：存取策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="48cf1-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="48cf1-144">`[EnvironmentName <String>]`：環境名稱</span><span class="sxs-lookup"><span data-stu-id="48cf1-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="48cf1-145">`[EventSourceName <String>]`：與指定環境相關聯的時間序列深入資訊事件來源名稱。</span><span class="sxs-lookup"><span data-stu-id="48cf1-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="48cf1-146">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="48cf1-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="48cf1-147">`[ReferenceDataSetName <String>]`：參照資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="48cf1-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="48cf1-148">`[ResourceGroupName <String>]`：Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="48cf1-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="48cf1-149">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="48cf1-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="48cf1-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="48cf1-150">RELATED LINKS</span></span>

