---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 51cbe7cd6d4e08543feadb5ddd096330763b7236
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902685"
---
# <span data-ttu-id="8bcd9-101">New-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="8bcd9-101">New-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="8bcd9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8bcd9-102">SYNOPSIS</span></span>
<span data-ttu-id="8bcd9-103">在指定的訂閱和資源群組中建立環境。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-103">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="8bcd9-104">語法</span><span class="sxs-lookup"><span data-stu-id="8bcd9-104">SYNTAX</span></span>

### <span data-ttu-id="8bcd9-105">第 1 代 (預設) </span><span class="sxs-lookup"><span data-stu-id="8bcd9-105">Gen1 (Default)</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Capacity <Int32>
 -DataRetentionTime <TimeSpan> -Kind <Kind> -Location <String> -Sku <SkuName> [-SubscriptionId <String>]
 [-PartitionKeyProperty <ITimeSeriesIdProperty[]>] [-StorageLimitExceededBehavior <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8bcd9-106">第 2 代</span><span class="sxs-lookup"><span data-stu-id="8bcd9-106">Gen2</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Kind <Kind> -Location <String>
 -Sku <SkuName> -StorageAccountKey <SecureString> -StorageAccountName <String>
 -TimeSeriesIdProperty <ITimeSeriesIdProperty[]> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-WarmStoreDataRetentionTime <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="8bcd9-107">描述</span><span class="sxs-lookup"><span data-stu-id="8bcd9-107">DESCRIPTION</span></span>
<span data-ttu-id="8bcd9-108">在指定的訂閱和資源群組中建立環境。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-108">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="8bcd9-109">例子</span><span class="sxs-lookup"><span data-stu-id="8bcd9-109">EXAMPLES</span></span>

### <span data-ttu-id="8bcd9-110">範例 1：建立第 1 代時間序列深入資訊環境</span><span class="sxs-lookup"><span data-stu-id="8bcd9-110">Example 1: Create a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $TimeSpan = New-TimeSpan -Days 1 -Hours 1 -Minutes 25
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Kind Gen1 -Location eastus -Sku S1 -DataRetentionTime $TimeSpan -Capacity 2

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen1 eastus   tsitest001 2           S1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="8bcd9-111">此命令會建立第 1 代時間序列深入資訊環境。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-111">This command creates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="8bcd9-112">範例 2：建立第 2 代時間序列深入資訊環境</span><span class="sxs-lookup"><span data-stu-id="8bcd9-112">Example 2: Create a Gen2 time series insights environment</span></span>
```powershell
PS C:\> $ks = Get-AzStorageAccountKey -ResourceGroupName "testgroup" -Name "staccount001"
PS C:\> $k  = $ks[0].Value | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest002 -Kind Gen2 -Location eastus -Sku L1 -StorageAccountName staccount001 -StorageAccountKey $k -TimeSeriesIdProperty @{name='cdc';type='string'}

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen2 eastus   tsitest002 1           L1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="8bcd9-113">此命令會建立第 2 代時間序列深入資訊環境。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-113">This command creates a Gen2 time series insights environment.</span></span>

## <span data-ttu-id="8bcd9-114">參數</span><span class="sxs-lookup"><span data-stu-id="8bcd9-114">PARAMETERS</span></span>

### <span data-ttu-id="8bcd9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8bcd9-115">-AsJob</span></span>
<span data-ttu-id="8bcd9-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="8bcd9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8bcd9-117">-容量</span><span class="sxs-lookup"><span data-stu-id="8bcd9-117">-Capacity</span></span>
<span data-ttu-id="8bcd9-118">SKU 的容量。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-118">The capacity of the sku.</span></span>
<span data-ttu-id="8bcd9-119">對於第 1 代環境，此值可以在建立後支援縮小環境。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-119">For Gen1 environments, this value can be changed to support scale out of environments after they have been created.</span></span>

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

### <span data-ttu-id="8bcd9-120">-DataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="8bcd9-120">-DataRetentionTime</span></span>
<span data-ttu-id="8bcd9-121">資料保留時間。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-121">The data retention time.</span></span>

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

### <span data-ttu-id="8bcd9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bcd9-122">-DefaultProfile</span></span>
<span data-ttu-id="8bcd9-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bcd9-124">-Kind</span><span class="sxs-lookup"><span data-stu-id="8bcd9-124">-Kind</span></span>
<span data-ttu-id="8bcd9-125">這是一種環境。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-125">The kind of the environment.</span></span>

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

### <span data-ttu-id="8bcd9-126">-位置</span><span class="sxs-lookup"><span data-stu-id="8bcd9-126">-Location</span></span>
<span data-ttu-id="8bcd9-127">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-127">The location of the resource.</span></span>

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

### <span data-ttu-id="8bcd9-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="8bcd9-128">-Name</span></span>
<span data-ttu-id="8bcd9-129">環境名稱</span><span class="sxs-lookup"><span data-stu-id="8bcd9-129">Name of the environment</span></span>

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

### <span data-ttu-id="8bcd9-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8bcd9-130">-NoWait</span></span>
<span data-ttu-id="8bcd9-131">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="8bcd9-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8bcd9-132">-PartitionKeyProperty</span><span class="sxs-lookup"><span data-stu-id="8bcd9-132">-PartitionKeyProperty</span></span>
<span data-ttu-id="8bcd9-133">將用來分割環境中資料的事件屬性清單。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-133">The list of event properties which will be used to partition data in the environment.</span></span>
<span data-ttu-id="8bcd9-134">若要建構，請參閱 PARTITIONKEYPROPERTY 屬性的附注區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-134">To construct, see NOTES section for PARTITIONKEYPROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="8bcd9-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bcd9-135">-ResourceGroupName</span></span>
<span data-ttu-id="8bcd9-136">Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="8bcd9-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="8bcd9-137">-Sku</span></span>
<span data-ttu-id="8bcd9-138">此 SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-138">The name of this SKU.</span></span>

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

### <span data-ttu-id="8bcd9-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="8bcd9-139">-StorageAccountKey</span></span>
<span data-ttu-id="8bcd9-140">授予時間系列深入資訊服務寫入存取儲存帳戶之管理金鑰的值。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-140">The value of the management key that grants the Time Series Insights service write access to the storage account.</span></span>

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

### <span data-ttu-id="8bcd9-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8bcd9-141">-StorageAccountName</span></span>
<span data-ttu-id="8bcd9-142">存放環境長期資料的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-142">The name of the storage account that will hold the environment's long term data.</span></span>

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

### <span data-ttu-id="8bcd9-143">-StorageLimitExceedEdBehavior</span><span class="sxs-lookup"><span data-stu-id="8bcd9-143">-StorageLimitExceededBehavior</span></span>
<span data-ttu-id="8bcd9-144">時間序列深入資訊服務在超過環境容量時應該採取的行為</span><span class="sxs-lookup"><span data-stu-id="8bcd9-144">The behavior the Time Series Insights service should take when the environment's capacity has been exceeded</span></span>

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

### <span data-ttu-id="8bcd9-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8bcd9-145">-SubscriptionId</span></span>
<span data-ttu-id="8bcd9-146">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-146">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="8bcd9-147">-標記</span><span class="sxs-lookup"><span data-stu-id="8bcd9-147">-Tag</span></span>
<span data-ttu-id="8bcd9-148">資源的其他屬性的金鑰值組。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-148">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="8bcd9-149">-TimeSeriesIdProperty</span><span class="sxs-lookup"><span data-stu-id="8bcd9-149">-TimeSeriesIdProperty</span></span>
<span data-ttu-id="8bcd9-150">將用來定義環境的時間序列識別碼的事件屬性清單。若要建構，請參閱 TIMESERIESIDPROPERTY 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-150">The list of event properties which will be used to define the environment's time series id. To construct, see NOTES section for TIMESERIESIDPROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="8bcd9-151">-WarmStoreDataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="8bcd9-151">-WarmStoreDataRetentionTime</span></span>
<span data-ttu-id="8bcd9-152">ISO8601 時間範圍指定環境事件可從暖區查詢的天數。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-152">ISO8601 timespan specifying the number of days the environment's events will be available for query from the warm store.</span></span>

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

### <span data-ttu-id="8bcd9-153">-確認</span><span class="sxs-lookup"><span data-stu-id="8bcd9-153">-Confirm</span></span>
<span data-ttu-id="8bcd9-154">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bcd9-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bcd9-155">-WhatIf</span></span>
<span data-ttu-id="8bcd9-156">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bcd9-157">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bcd9-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bcd9-158">CommonParameters</span></span>
<span data-ttu-id="8bcd9-159">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bcd9-160">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8bcd9-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bcd9-161">輸入</span><span class="sxs-lookup"><span data-stu-id="8bcd9-161">INPUTS</span></span>

## <span data-ttu-id="8bcd9-162">輸出</span><span class="sxs-lookup"><span data-stu-id="8bcd9-162">OUTPUTS</span></span>

### <span data-ttu-id="8bcd9-163">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="8bcd9-163">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="8bcd9-164">筆記</span><span class="sxs-lookup"><span data-stu-id="8bcd9-164">NOTES</span></span>

<span data-ttu-id="8bcd9-165">別名</span><span class="sxs-lookup"><span data-stu-id="8bcd9-165">ALIASES</span></span>

<span data-ttu-id="8bcd9-166">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="8bcd9-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8bcd9-167">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8bcd9-168">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8bcd9-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>：用於分割環境中資料的事件屬性清單。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to partition data in the environment.</span></span>
  - <span data-ttu-id="8bcd9-170">`[Name <String>]`：屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-170">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="8bcd9-171">`[Type <PropertyType?>]`：屬性的類型。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-171">`[Type <PropertyType?>]`: The type of the property.</span></span>

<span data-ttu-id="8bcd9-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>：將用來定義環境時間序列識別碼的事件屬性清單。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to define the environment's time series id.</span></span>
  - <span data-ttu-id="8bcd9-173">`[Name <String>]`：屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-173">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="8bcd9-174">`[Type <PropertyType?>]`：屬性的類型。</span><span class="sxs-lookup"><span data-stu-id="8bcd9-174">`[Type <PropertyType?>]`: The type of the property.</span></span>

## <span data-ttu-id="8bcd9-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="8bcd9-175">RELATED LINKS</span></span>

