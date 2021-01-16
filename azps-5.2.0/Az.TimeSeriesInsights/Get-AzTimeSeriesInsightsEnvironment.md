---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: f4f42b257c5ce54085214c8cd9d2f79d9e8a6387
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284728"
---
# <span data-ttu-id="de65a-101">Get-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="de65a-101">Get-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="de65a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="de65a-102">SYNOPSIS</span></span>
<span data-ttu-id="de65a-103">在指定的訂閱和資源群組中，取得具有指定名稱的環境。</span><span class="sxs-lookup"><span data-stu-id="de65a-103">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="de65a-104">句法</span><span class="sxs-lookup"><span data-stu-id="de65a-104">SYNTAX</span></span>

### <span data-ttu-id="de65a-105">List1 (預設) </span><span class="sxs-lookup"><span data-stu-id="de65a-105">List1 (Default)</span></span>
```
Get-AzTimeSeriesInsightsEnvironment [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="de65a-106">獲取</span><span class="sxs-lookup"><span data-stu-id="de65a-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="de65a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="de65a-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="de65a-108">清單</span><span class="sxs-lookup"><span data-stu-id="de65a-108">List</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="de65a-109">說明</span><span class="sxs-lookup"><span data-stu-id="de65a-109">DESCRIPTION</span></span>
<span data-ttu-id="de65a-110">在指定的訂閱和資源群組中，取得具有指定名稱的環境。</span><span class="sxs-lookup"><span data-stu-id="de65a-110">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="de65a-111">示例</span><span class="sxs-lookup"><span data-stu-id="de65a-111">EXAMPLES</span></span>

### <span data-ttu-id="de65a-112">範例1：取得時序深入分析環境</span><span class="sxs-lookup"><span data-stu-id="de65a-112">Example 1: Get a time series insights environment</span></span>
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

<span data-ttu-id="de65a-113">這個命令會取得時序深入分析環境。</span><span class="sxs-lookup"><span data-stu-id="de65a-113">This command gets a time series insights environment.</span></span>

### <span data-ttu-id="de65a-114">範例2：列出所有時序深入分析環境</span><span class="sxs-lookup"><span data-stu-id="de65a-114">Example 2: List all time series insights environments</span></span>
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

<span data-ttu-id="de65a-115">這個命令會列出資源群組中的所有時序深入分析環境。</span><span class="sxs-lookup"><span data-stu-id="de65a-115">This command lists all time series insights environments in a resource group.</span></span>

### <span data-ttu-id="de65a-116">範例3：透過物件取得時序分析真知灼見環境</span><span class="sxs-lookup"><span data-stu-id="de65a-116">Example 3: Get a time series insights environment by object</span></span>
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

<span data-ttu-id="de65a-117">這個命令會取得時序深入分析環境。</span><span class="sxs-lookup"><span data-stu-id="de65a-117">This command gets a time series insights environments.</span></span>

## <span data-ttu-id="de65a-118">參數</span><span class="sxs-lookup"><span data-stu-id="de65a-118">PARAMETERS</span></span>

### <span data-ttu-id="de65a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de65a-119">-DefaultProfile</span></span>
<span data-ttu-id="de65a-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="de65a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de65a-121">-展開</span><span class="sxs-lookup"><span data-stu-id="de65a-121">-Expand</span></span>
<span data-ttu-id="de65a-122">設定 $expand = status 會將環境的內部服務狀態包含在時間序列 Insights 服務中。</span><span class="sxs-lookup"><span data-stu-id="de65a-122">Setting $expand=status will include the status of the internal services of the environment in the Time Series Insights service.</span></span>

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

### <span data-ttu-id="de65a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de65a-123">-InputObject</span></span>
<span data-ttu-id="de65a-124">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="de65a-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="de65a-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="de65a-125">-Name</span></span>
<span data-ttu-id="de65a-126">與指定的資源群組相關聯之時間序列 Insights 環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="de65a-126">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="de65a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de65a-127">-ResourceGroupName</span></span>
<span data-ttu-id="de65a-128">Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="de65a-128">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="de65a-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="de65a-129">-SubscriptionId</span></span>
<span data-ttu-id="de65a-130">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="de65a-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="de65a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de65a-131">CommonParameters</span></span>
<span data-ttu-id="de65a-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="de65a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de65a-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="de65a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de65a-134">輸入</span><span class="sxs-lookup"><span data-stu-id="de65a-134">INPUTS</span></span>

### <span data-ttu-id="de65a-135">ITimeSeriesInsightsIdentity （TimeSeriesInsights）的</span><span class="sxs-lookup"><span data-stu-id="de65a-135">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="de65a-136">輸出</span><span class="sxs-lookup"><span data-stu-id="de65a-136">OUTPUTS</span></span>

### <span data-ttu-id="de65a-137">IEnvironmentResource （TimeSeriesInsights）。 Api20200515。</span><span class="sxs-lookup"><span data-stu-id="de65a-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="de65a-138">筆記</span><span class="sxs-lookup"><span data-stu-id="de65a-138">NOTES</span></span>

<span data-ttu-id="de65a-139">別名</span><span class="sxs-lookup"><span data-stu-id="de65a-139">ALIASES</span></span>

<span data-ttu-id="de65a-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="de65a-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="de65a-141">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="de65a-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="de65a-142">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="de65a-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="de65a-143">INPUTOBJECT <ITimeSeriesInsightsIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="de65a-143">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="de65a-144">`[AccessPolicyName <String>]`：存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="de65a-144">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="de65a-145">`[EnvironmentName <String>]`：環境的名稱</span><span class="sxs-lookup"><span data-stu-id="de65a-145">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="de65a-146">`[EventSourceName <String>]`：與指定環境相關聯之時間序列 Insights 事件來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="de65a-146">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="de65a-147">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="de65a-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="de65a-148">`[ReferenceDataSetName <String>]`：參照資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="de65a-148">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="de65a-149">`[ResourceGroupName <String>]`： Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="de65a-149">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="de65a-150">`[SubscriptionId <String>]`： Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="de65a-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="de65a-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="de65a-151">RELATED LINKS</span></span>

