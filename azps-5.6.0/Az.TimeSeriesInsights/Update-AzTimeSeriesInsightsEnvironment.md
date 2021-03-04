---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 86e143455f287bef8bff4b391f7f40aa01fba99b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910890"
---
# <span data-ttu-id="00935-101">Update-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="00935-101">Update-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="00935-102">簡介</span><span class="sxs-lookup"><span data-stu-id="00935-102">SYNOPSIS</span></span>
<span data-ttu-id="00935-103">以指定的訂閱和資源群組中的指定名稱更新環境。</span><span class="sxs-lookup"><span data-stu-id="00935-103">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="00935-104">語法</span><span class="sxs-lookup"><span data-stu-id="00935-104">SYNTAX</span></span>

### <span data-ttu-id="00935-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="00935-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="00935-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="00935-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="00935-107">描述</span><span class="sxs-lookup"><span data-stu-id="00935-107">DESCRIPTION</span></span>
<span data-ttu-id="00935-108">以指定的訂閱和資源群組中的指定名稱更新環境。</span><span class="sxs-lookup"><span data-stu-id="00935-108">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="00935-109">例子</span><span class="sxs-lookup"><span data-stu-id="00935-109">EXAMPLES</span></span>

### <span data-ttu-id="00935-110">範例 1：更新第 1 代時間序列深入資訊環境</span><span class="sxs-lookup"><span data-stu-id="00935-110">Example 1: Update a Gen1 time series insights environment</span></span>
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

<span data-ttu-id="00935-111">此命令會更新第 1 代時間序列深入資訊環境。</span><span class="sxs-lookup"><span data-stu-id="00935-111">This command updates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="00935-112">範例 2：更新第 1 代時間序列深入資訊環境</span><span class="sxs-lookup"><span data-stu-id="00935-112">Example 2:  Update a Gen1 time series insights environment</span></span>
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

<span data-ttu-id="00935-113">此命令會更新第 1 代時間序列深入資訊環境。</span><span class="sxs-lookup"><span data-stu-id="00935-113">This command updates a Gen1 time series insights environment.</span></span>

## <span data-ttu-id="00935-114">參數</span><span class="sxs-lookup"><span data-stu-id="00935-114">PARAMETERS</span></span>

### <span data-ttu-id="00935-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00935-115">-AsJob</span></span>
<span data-ttu-id="00935-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="00935-116">Run the command as a job</span></span>

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

### <span data-ttu-id="00935-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00935-117">-DefaultProfile</span></span>
<span data-ttu-id="00935-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="00935-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00935-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00935-119">-InputObject</span></span>
<span data-ttu-id="00935-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="00935-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="00935-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="00935-121">-Name</span></span>
<span data-ttu-id="00935-122">與指定資源群組相關聯的時間序列深入資訊環境名稱。</span><span class="sxs-lookup"><span data-stu-id="00935-122">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="00935-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="00935-123">-NoWait</span></span>
<span data-ttu-id="00935-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="00935-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="00935-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00935-125">-ResourceGroupName</span></span>
<span data-ttu-id="00935-126">Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="00935-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="00935-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="00935-127">-SubscriptionId</span></span>
<span data-ttu-id="00935-128">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="00935-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="00935-129">-標記</span><span class="sxs-lookup"><span data-stu-id="00935-129">-Tag</span></span>
<span data-ttu-id="00935-130">環境其他屬性的金鑰值組。</span><span class="sxs-lookup"><span data-stu-id="00935-130">Key-value pairs of additional properties for the environment.</span></span>

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

### <span data-ttu-id="00935-131">-確認</span><span class="sxs-lookup"><span data-stu-id="00935-131">-Confirm</span></span>
<span data-ttu-id="00935-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="00935-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00935-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00935-133">-WhatIf</span></span>
<span data-ttu-id="00935-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="00935-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00935-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="00935-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00935-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00935-136">CommonParameters</span></span>
<span data-ttu-id="00935-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="00935-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00935-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00935-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00935-139">輸入</span><span class="sxs-lookup"><span data-stu-id="00935-139">INPUTS</span></span>

### <span data-ttu-id="00935-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="00935-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="00935-141">輸出</span><span class="sxs-lookup"><span data-stu-id="00935-141">OUTPUTS</span></span>

### <span data-ttu-id="00935-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="00935-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="00935-143">筆記</span><span class="sxs-lookup"><span data-stu-id="00935-143">NOTES</span></span>

<span data-ttu-id="00935-144">別名</span><span class="sxs-lookup"><span data-stu-id="00935-144">ALIASES</span></span>

<span data-ttu-id="00935-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="00935-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="00935-146">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="00935-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="00935-147">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="00935-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="00935-148">INPUTOBJECT： <ITimeSeriesInsightsIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="00935-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="00935-149">`[AccessPolicyName <String>]`：存取策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="00935-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="00935-150">`[EnvironmentName <String>]`：環境名稱</span><span class="sxs-lookup"><span data-stu-id="00935-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="00935-151">`[EventSourceName <String>]`：與指定環境相關聯的時間序列深入資訊事件來源名稱。</span><span class="sxs-lookup"><span data-stu-id="00935-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="00935-152">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="00935-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="00935-153">`[ReferenceDataSetName <String>]`：參照資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="00935-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="00935-154">`[ResourceGroupName <String>]`：Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="00935-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="00935-155">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="00935-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="00935-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="00935-156">RELATED LINKS</span></span>

