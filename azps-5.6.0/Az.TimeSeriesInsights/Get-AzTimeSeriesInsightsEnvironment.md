---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 151b8a431183727dbfaec242705421ba775b0b99
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916820"
---
# <span data-ttu-id="05be7-101">Get-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="05be7-101">Get-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="05be7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="05be7-102">SYNOPSIS</span></span>
<span data-ttu-id="05be7-103">在指定的訂閱和資源群組中，以指定的名稱獲取環境。</span><span class="sxs-lookup"><span data-stu-id="05be7-103">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="05be7-104">語法</span><span class="sxs-lookup"><span data-stu-id="05be7-104">SYNTAX</span></span>

### <span data-ttu-id="05be7-105">清單1 (預設) </span><span class="sxs-lookup"><span data-stu-id="05be7-105">List1 (Default)</span></span>
```
Get-AzTimeSeriesInsightsEnvironment [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="05be7-106">獲取</span><span class="sxs-lookup"><span data-stu-id="05be7-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="05be7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="05be7-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="05be7-108">清單</span><span class="sxs-lookup"><span data-stu-id="05be7-108">List</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="05be7-109">描述</span><span class="sxs-lookup"><span data-stu-id="05be7-109">DESCRIPTION</span></span>
<span data-ttu-id="05be7-110">在指定的訂閱和資源群組中，以指定的名稱獲取環境。</span><span class="sxs-lookup"><span data-stu-id="05be7-110">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="05be7-111">例子</span><span class="sxs-lookup"><span data-stu-id="05be7-111">EXAMPLES</span></span>

### <span data-ttu-id="05be7-112">範例 1：取得時間序列深入資訊環境</span><span class="sxs-lookup"><span data-stu-id="05be7-112">Example 1: Get a time series insights environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001

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
SkuCapacity                  : 2
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="05be7-113">此命令會獲得時間序列深入資訊環境。</span><span class="sxs-lookup"><span data-stu-id="05be7-113">This command gets a time series insights environment.</span></span>

### <span data-ttu-id="05be7-114">範例 2：列出所有時間序列深入資訊環境</span><span class="sxs-lookup"><span data-stu-id="05be7-114">Example 2: List all time series insights environments</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup

DataAccessFqdn                      : 3de1d1e1-4f9b-4bc6-aad3-a835597dcd86.env.timeseries.azure.com
DataAccessId                        : 3de1d1e1-4f9b-4bc6-aad3-a835597dcd86
Id                                  : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/ 
                                      tsill
IngressState                        :
Kind                                : Gen2
Location                            : EastUs
Name                                : tsill
PropertyUsageState                  :
Sku                                 : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                         : 1
SkuName                             : L1
StateDetailCode                     :
StateDetailCurrentCount             :
StateDetailMaxCount                 :
StateDetailMessage                  :
StorageConfigurationAccountName     : cdolauli
Tag                                 : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimeSeriesIdProperty                : {ccc}
Type                                : Microsoft.TimeSeriesInsights/Environments
WarmStoreConfigurationDataRetention : 00:00:00

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
SkuCapacity                  : 2
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="05be7-115">此命令會列出資源群組中所有時間序列深入資訊環境。</span><span class="sxs-lookup"><span data-stu-id="05be7-115">This command lists all time series insights environments in a resource group.</span></span>

### <span data-ttu-id="05be7-116">範例 3：根據物件取得時間序列深入資訊環境</span><span class="sxs-lookup"><span data-stu-id="05be7-116">Example 3: Get a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName tsi-test-i01k5l -Name tsi-envv8u56x 
PS C:\> Get-AzTimeSeriesInsightsEnvironment -InputObject $env

DataAccessFqdn               : d76a61f2-8a30-41a5-9587-f241eb9b48d9.env.timeseries.azure.com
DataAccessId                 : d76a61f2-8a30-41a5-9587-f241eb9b48d9
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.TimeSeriesInsights/environments/tsi-envv8u56x
IngressState                 :
Kind                         : Gen1
Location                     : eastus2
Name                         : tsi-envv8u56x
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 1
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="05be7-117">此命令會獲得時間序列深入資訊環境。</span><span class="sxs-lookup"><span data-stu-id="05be7-117">This command gets a time series insights environments.</span></span>

## <span data-ttu-id="05be7-118">參數</span><span class="sxs-lookup"><span data-stu-id="05be7-118">PARAMETERS</span></span>

### <span data-ttu-id="05be7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05be7-119">-DefaultProfile</span></span>
<span data-ttu-id="05be7-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="05be7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05be7-121">-展開</span><span class="sxs-lookup"><span data-stu-id="05be7-121">-Expand</span></span>
<span data-ttu-id="05be7-122">設定 $expand=status 會包含時間系列深入資訊服務中的環境內部服務狀態。</span><span class="sxs-lookup"><span data-stu-id="05be7-122">Setting $expand=status will include the status of the internal services of the environment in the Time Series Insights service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05be7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05be7-123">-InputObject</span></span>
<span data-ttu-id="05be7-124">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="05be7-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="05be7-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="05be7-125">-Name</span></span>
<span data-ttu-id="05be7-126">與指定資源群組相關聯的時間序列深入資訊環境名稱。</span><span class="sxs-lookup"><span data-stu-id="05be7-126">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05be7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05be7-127">-ResourceGroupName</span></span>
<span data-ttu-id="05be7-128">Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="05be7-128">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="05be7-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05be7-129">-SubscriptionId</span></span>
<span data-ttu-id="05be7-130">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="05be7-130">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05be7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05be7-131">CommonParameters</span></span>
<span data-ttu-id="05be7-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="05be7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05be7-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05be7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05be7-134">輸入</span><span class="sxs-lookup"><span data-stu-id="05be7-134">INPUTS</span></span>

### <span data-ttu-id="05be7-135">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="05be7-135">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="05be7-136">輸出</span><span class="sxs-lookup"><span data-stu-id="05be7-136">OUTPUTS</span></span>

### <span data-ttu-id="05be7-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="05be7-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="05be7-138">筆記</span><span class="sxs-lookup"><span data-stu-id="05be7-138">NOTES</span></span>

<span data-ttu-id="05be7-139">別名</span><span class="sxs-lookup"><span data-stu-id="05be7-139">ALIASES</span></span>

<span data-ttu-id="05be7-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="05be7-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="05be7-141">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="05be7-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="05be7-142">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="05be7-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="05be7-143">INPUTOBJECT： <ITimeSeriesInsightsIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="05be7-143">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="05be7-144">`[AccessPolicyName <String>]`：存取策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="05be7-144">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="05be7-145">`[EnvironmentName <String>]`：環境名稱</span><span class="sxs-lookup"><span data-stu-id="05be7-145">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="05be7-146">`[EventSourceName <String>]`：與指定環境相關聯的時間序列深入資訊事件來源名稱。</span><span class="sxs-lookup"><span data-stu-id="05be7-146">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="05be7-147">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="05be7-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="05be7-148">`[ReferenceDataSetName <String>]`：參照資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="05be7-148">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="05be7-149">`[ResourceGroupName <String>]`：Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="05be7-149">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="05be7-150">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="05be7-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="05be7-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="05be7-151">RELATED LINKS</span></span>

