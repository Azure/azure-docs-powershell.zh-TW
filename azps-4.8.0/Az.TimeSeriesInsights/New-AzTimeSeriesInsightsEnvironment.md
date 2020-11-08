---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: b4f27c31ebc3eb54727d6df1139409529c20eed9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129387"
---
# <span data-ttu-id="8c9b9-101">New-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="8c9b9-101">New-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="8c9b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c9b9-102">SYNOPSIS</span></span>
<span data-ttu-id="8c9b9-103">在指定的訂閱和資源群組中建立環境。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-103">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="8c9b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c9b9-104">SYNTAX</span></span>

### <span data-ttu-id="8c9b9-105">Gen1 (預設) </span><span class="sxs-lookup"><span data-stu-id="8c9b9-105">Gen1 (Default)</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Capacity <Int32>
 -DataRetentionTime <TimeSpan> -Kind <Kind> -Location <String> -Sku <SkuName> [-SubscriptionId <String>]
 [-PartitionKeyProperty <ITimeSeriesIdProperty[]>] [-StorageLimitExceededBehavior <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8c9b9-106">Gen2</span><span class="sxs-lookup"><span data-stu-id="8c9b9-106">Gen2</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Kind <Kind> -Location <String>
 -Sku <SkuName> -StorageAccountKey <SecureString> -StorageAccountName <String>
 -TimeSeriesIdProperty <ITimeSeriesIdProperty[]> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-WarmStoreDataRetentionTime <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="8c9b9-107">說明</span><span class="sxs-lookup"><span data-stu-id="8c9b9-107">DESCRIPTION</span></span>
<span data-ttu-id="8c9b9-108">在指定的訂閱和資源群組中建立環境。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-108">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="8c9b9-109">示例</span><span class="sxs-lookup"><span data-stu-id="8c9b9-109">EXAMPLES</span></span>

### <span data-ttu-id="8c9b9-110">範例1：建立 Gen1 時序分析環境</span><span class="sxs-lookup"><span data-stu-id="8c9b9-110">Example 1: Create a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $TimeSpan = New-TimeSpan -Days 1 -Hours 1 -Minutes 25
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Kind Gen1 -Location eastus -Sku S1 -DataRetentionTime $TimeSpan -Capacity 2

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen1 eastus   tsitest001 2           S1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="8c9b9-111">這個命令會建立 Gen1 的時序深入分析環境。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-111">This command creates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="8c9b9-112">範例2：建立 Gen2 時序分析環境</span><span class="sxs-lookup"><span data-stu-id="8c9b9-112">Example 2: Create a Gen2 time series insights environment</span></span>
```powershell
PS C:\> $ks = Get-AzStorageAccountKey -ResourceGroupName "testgroup" -Name "staccount001"
PS C:\> $k  = $ks[0].Value | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest002 -Kind Gen2 -Location eastus -Sku L1 -StorageAccountName staccount001 -StorageAccountKey $k -TimeSeriesIdProperty @{name='cdc';type='string'}

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen2 eastus   tsitest002 1           L1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="8c9b9-113">這個命令會建立 Gen2 的時序深入分析環境。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-113">This command creates a Gen2 time series insights environment.</span></span>

## <span data-ttu-id="8c9b9-114">參數</span><span class="sxs-lookup"><span data-stu-id="8c9b9-114">PARAMETERS</span></span>

### <span data-ttu-id="8c9b9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c9b9-115">-AsJob</span></span>
<span data-ttu-id="8c9b9-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="8c9b9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8c9b9-117">-容量</span><span class="sxs-lookup"><span data-stu-id="8c9b9-117">-Capacity</span></span>
<span data-ttu-id="8c9b9-118">Sku 的容量。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-118">The capacity of the sku.</span></span>
<span data-ttu-id="8c9b9-119">針對 Gen1 環境，您可以將這個值變更為支援在已建立環境之後，擴大規模。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-119">For Gen1 environments, this value can be changed to support scale out of environments after they have been created.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Gen1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9b9-120">-DataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="8c9b9-120">-DataRetentionTime</span></span>
<span data-ttu-id="8c9b9-121">資料保留時間。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-121">The data retention time.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Gen1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9b9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c9b9-122">-DefaultProfile</span></span>
<span data-ttu-id="8c9b9-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c9b9-124">類型</span><span class="sxs-lookup"><span data-stu-id="8c9b9-124">-Kind</span></span>
<span data-ttu-id="8c9b9-125">環境的類型。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-125">The kind of the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9b9-126">-位置</span><span class="sxs-lookup"><span data-stu-id="8c9b9-126">-Location</span></span>
<span data-ttu-id="8c9b9-127">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-127">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9b9-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="8c9b9-128">-Name</span></span>
<span data-ttu-id="8c9b9-129">環境名稱</span><span class="sxs-lookup"><span data-stu-id="8c9b9-129">Name of the environment</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9b9-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8c9b9-130">-NoWait</span></span>
<span data-ttu-id="8c9b9-131">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="8c9b9-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8c9b9-132">-PartitionKeyProperty</span><span class="sxs-lookup"><span data-stu-id="8c9b9-132">-PartitionKeyProperty</span></span>
<span data-ttu-id="8c9b9-133">將用來在環境中對資料進行分區的事件屬性清單。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-133">The list of event properties which will be used to partition data in the environment.</span></span>
<span data-ttu-id="8c9b9-134">若要建立，請參閱 PARTITIONKEYPROPERTY 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-134">To construct, see NOTES section for PARTITIONKEYPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.ITimeSeriesIdProperty[]
Parameter Sets: Gen1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9b9-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c9b9-135">-ResourceGroupName</span></span>
<span data-ttu-id="8c9b9-136">Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-136">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9b9-137">-Sku</span><span class="sxs-lookup"><span data-stu-id="8c9b9-137">-Sku</span></span>
<span data-ttu-id="8c9b9-138">這個 SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-138">The name of this SKU.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9b9-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="8c9b9-139">-StorageAccountKey</span></span>
<span data-ttu-id="8c9b9-140">提供存儲帳戶寫入時間數列 Insights 服務寫入存取權的管理金鑰值。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-140">The value of the management key that grants the Time Series Insights service write access to the storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9b9-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8c9b9-141">-StorageAccountName</span></span>
<span data-ttu-id="8c9b9-142">儲存在環境長期資料中的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-142">The name of the storage account that will hold the environment's long term data.</span></span>

```yaml
Type: System.String
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9b9-143">-StorageLimitExceededBehavior</span><span class="sxs-lookup"><span data-stu-id="8c9b9-143">-StorageLimitExceededBehavior</span></span>
<span data-ttu-id="8c9b9-144">在超出環境容量的情況下，時間序列 Insights 服務應採取的行為</span><span class="sxs-lookup"><span data-stu-id="8c9b9-144">The behavior the Time Series Insights service should take when the environment's capacity has been exceeded</span></span>

```yaml
Type: System.String
Parameter Sets: Gen1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9b9-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8c9b9-145">-SubscriptionId</span></span>
<span data-ttu-id="8c9b9-146">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-146">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9b9-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="8c9b9-147">-Tag</span></span>
<span data-ttu-id="8c9b9-148">資源之其他屬性的鍵值對。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-148">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="8c9b9-149">-TimeSeriesIdProperty</span><span class="sxs-lookup"><span data-stu-id="8c9b9-149">-TimeSeriesIdProperty</span></span>
<span data-ttu-id="8c9b9-150">事件屬性的清單，將用來定義環境的時間序列 id。若要建立，請參閱 TIMESERIESIDPROPERTY 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-150">The list of event properties which will be used to define the environment's time series id. To construct, see NOTES section for TIMESERIESIDPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.ITimeSeriesIdProperty[]
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9b9-151">-WarmStoreDataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="8c9b9-151">-WarmStoreDataRetentionTime</span></span>
<span data-ttu-id="8c9b9-152">ISO8601 timespan 指定環境事件將可供來自暖存放區之查詢的天數。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-152">ISO8601 timespan specifying the number of days the environment's events will be available for query from the warm store.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Gen2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9b9-153">-確認</span><span class="sxs-lookup"><span data-stu-id="8c9b9-153">-Confirm</span></span>
<span data-ttu-id="8c9b9-154">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c9b9-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c9b9-155">-WhatIf</span></span>
<span data-ttu-id="8c9b9-156">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c9b9-157">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c9b9-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c9b9-158">CommonParameters</span></span>
<span data-ttu-id="8c9b9-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c9b9-160">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c9b9-161">輸入</span><span class="sxs-lookup"><span data-stu-id="8c9b9-161">INPUTS</span></span>

## <span data-ttu-id="8c9b9-162">輸出</span><span class="sxs-lookup"><span data-stu-id="8c9b9-162">OUTPUTS</span></span>

### <span data-ttu-id="8c9b9-163">IEnvironmentResource （TimeSeriesInsights）。 Api20200515。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-163">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="8c9b9-164">筆記</span><span class="sxs-lookup"><span data-stu-id="8c9b9-164">NOTES</span></span>

<span data-ttu-id="8c9b9-165">別名</span><span class="sxs-lookup"><span data-stu-id="8c9b9-165">ALIASES</span></span>

<span data-ttu-id="8c9b9-166">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="8c9b9-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8c9b9-167">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8c9b9-168">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8c9b9-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty [] >：將用來在環境中劃分資料的事件屬性清單。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to partition data in the environment.</span></span>
  - <span data-ttu-id="8c9b9-170">`[Name <String>]`：屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-170">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="8c9b9-171">`[Type <PropertyType?>]`：屬性的類型。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-171">`[Type <PropertyType?>]`: The type of the property.</span></span>

<span data-ttu-id="8c9b9-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty [] >：將用來定義環境的時間序列 id 的事件屬性清單。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to define the environment's time series id.</span></span>
  - <span data-ttu-id="8c9b9-173">`[Name <String>]`：屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-173">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="8c9b9-174">`[Type <PropertyType?>]`：屬性的類型。</span><span class="sxs-lookup"><span data-stu-id="8c9b9-174">`[Type <PropertyType?>]`: The type of the property.</span></span>

## <span data-ttu-id="8c9b9-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c9b9-175">RELATED LINKS</span></span>

