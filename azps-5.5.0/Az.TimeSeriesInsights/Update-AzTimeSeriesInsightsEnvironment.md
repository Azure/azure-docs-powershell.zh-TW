---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: e2b7fa000251a12e09dfd7cd345f54f967962839
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142818"
---
# <span data-ttu-id="6c2e1-101">Update-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="6c2e1-101">Update-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="6c2e1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6c2e1-102">SYNOPSIS</span></span>
<span data-ttu-id="6c2e1-103">在指定的訂閱和資源群組中，更新具有指定名稱的環境。</span><span class="sxs-lookup"><span data-stu-id="6c2e1-103">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="6c2e1-104">句法</span><span class="sxs-lookup"><span data-stu-id="6c2e1-104">SYNTAX</span></span>

### <span data-ttu-id="6c2e1-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="6c2e1-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6c2e1-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6c2e1-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6c2e1-107">說明</span><span class="sxs-lookup"><span data-stu-id="6c2e1-107">DESCRIPTION</span></span>
<span data-ttu-id="6c2e1-108">在指定的訂閱和資源群組中，更新具有指定名稱的環境。</span><span class="sxs-lookup"><span data-stu-id="6c2e1-108">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="6c2e1-109">示例</span><span class="sxs-lookup"><span data-stu-id="6c2e1-109">EXAMPLES</span></span>

### <span data-ttu-id="6c2e1-110">範例1：更新 Gen1 時序分析環境</span><span class="sxs-lookup"><span data-stu-id="6c2e1-110">Example 1: Update a Gen1 time series insights environment</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Tag @{'key1'='val1'}

DataAccessFqdn               : b6d113a4-0865-405f-b09e-ad4355b5d046.env.timeseries.azure.com
DataAccessId                 : b6d113a4-0865-405f-b09e-ad4355b5d046
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest 
                               001
IngressState                 :
Kind                         : Gen1
Location                     : eastus
Name                         : tsitest001
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 5
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="6c2e1-111">這個命令會更新 Gen1 的時間序列 insights 環境。</span><span class="sxs-lookup"><span data-stu-id="6c2e1-111">This command updates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="6c2e1-112">範例2：更新 Gen1 時序分析環境</span><span class="sxs-lookup"><span data-stu-id="6c2e1-112">Example 2:  Update a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001
PS C:\> Update-AzTimeSeriesInsightsEnvironment -InputObject $env -Tag @{'key2'='val2'}

DataAccessFqdn               : b6d113a4-0865-405f-b09e-ad4355b5d046.env.timeseries.azure.com
DataAccessId                 : b6d113a4-0865-405f-b09e-ad4355b5d046
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest 
                               001
IngressState                 :
Kind                         : Gen1
Location                     : eastus
Name                         : tsitest001
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 5
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="6c2e1-113">這個命令會更新 Gen1 的時間序列 insights 環境。</span><span class="sxs-lookup"><span data-stu-id="6c2e1-113">This command updates a Gen1 time series insights environment.</span></span>

## <span data-ttu-id="6c2e1-114">參數</span><span class="sxs-lookup"><span data-stu-id="6c2e1-114">PARAMETERS</span></span>

### <span data-ttu-id="6c2e1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c2e1-115">-AsJob</span></span>
<span data-ttu-id="6c2e1-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="6c2e1-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6c2e1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c2e1-117">-DefaultProfile</span></span>
<span data-ttu-id="6c2e1-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6c2e1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c2e1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c2e1-119">-InputObject</span></span>
<span data-ttu-id="6c2e1-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6c2e1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c2e1-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="6c2e1-121">-Name</span></span>
<span data-ttu-id="6c2e1-122">與指定的資源群組相關聯之時間序列 Insights 環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c2e1-122">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c2e1-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6c2e1-123">-NoWait</span></span>
<span data-ttu-id="6c2e1-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="6c2e1-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6c2e1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c2e1-125">-ResourceGroupName</span></span>
<span data-ttu-id="6c2e1-126">Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c2e1-126">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c2e1-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6c2e1-127">-SubscriptionId</span></span>
<span data-ttu-id="6c2e1-128">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="6c2e1-128">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c2e1-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="6c2e1-129">-Tag</span></span>
<span data-ttu-id="6c2e1-130">環境之其他屬性的鍵值對。</span><span class="sxs-lookup"><span data-stu-id="6c2e1-130">Key-value pairs of additional properties for the environment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c2e1-131">-確認</span><span class="sxs-lookup"><span data-stu-id="6c2e1-131">-Confirm</span></span>
<span data-ttu-id="6c2e1-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6c2e1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c2e1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c2e1-133">-WhatIf</span></span>
<span data-ttu-id="6c2e1-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6c2e1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c2e1-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c2e1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c2e1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c2e1-136">CommonParameters</span></span>
<span data-ttu-id="6c2e1-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6c2e1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c2e1-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6c2e1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c2e1-139">輸入</span><span class="sxs-lookup"><span data-stu-id="6c2e1-139">INPUTS</span></span>

### <span data-ttu-id="6c2e1-140">ITimeSeriesInsightsIdentity （TimeSeriesInsights）的</span><span class="sxs-lookup"><span data-stu-id="6c2e1-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="6c2e1-141">輸出</span><span class="sxs-lookup"><span data-stu-id="6c2e1-141">OUTPUTS</span></span>

### <span data-ttu-id="6c2e1-142">IEnvironmentResource （TimeSeriesInsights）。 Api20200515。</span><span class="sxs-lookup"><span data-stu-id="6c2e1-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="6c2e1-143">筆記</span><span class="sxs-lookup"><span data-stu-id="6c2e1-143">NOTES</span></span>

<span data-ttu-id="6c2e1-144">別名</span><span class="sxs-lookup"><span data-stu-id="6c2e1-144">ALIASES</span></span>

<span data-ttu-id="6c2e1-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="6c2e1-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6c2e1-146">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="6c2e1-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6c2e1-147">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="6c2e1-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6c2e1-148">INPUTOBJECT <ITimeSeriesInsightsIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="6c2e1-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6c2e1-149">`[AccessPolicyName <String>]`：存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c2e1-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="6c2e1-150">`[EnvironmentName <String>]`：環境的名稱</span><span class="sxs-lookup"><span data-stu-id="6c2e1-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="6c2e1-151">`[EventSourceName <String>]`：與指定環境相關聯之時間序列 Insights 事件來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c2e1-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="6c2e1-152">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="6c2e1-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6c2e1-153">`[ReferenceDataSetName <String>]`：參照資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c2e1-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="6c2e1-154">`[ResourceGroupName <String>]`： Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c2e1-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="6c2e1-155">`[SubscriptionId <String>]`： Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="6c2e1-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="6c2e1-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c2e1-156">RELATED LINKS</span></span>

