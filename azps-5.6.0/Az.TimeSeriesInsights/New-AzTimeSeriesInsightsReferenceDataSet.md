---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 1c4e0fa2a8e204ee3b0dad160d3cfb54f58b4323
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907934"
---
# <span data-ttu-id="d7a9a-101">New-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="d7a9a-101">New-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="d7a9a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d7a9a-102">SYNOPSIS</span></span>
<span data-ttu-id="d7a9a-103">在指定的環境中建立或更新參照資料集。</span><span class="sxs-lookup"><span data-stu-id="d7a9a-103">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="d7a9a-104">語法</span><span class="sxs-lookup"><span data-stu-id="d7a9a-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -KeyProperty <IReferenceDataSetKeyProperty[]> -Location <String> [-SubscriptionId <String>]
 [-DataStringComparisonBehavior <DataStringComparisonBehavior>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d7a9a-105">描述</span><span class="sxs-lookup"><span data-stu-id="d7a9a-105">DESCRIPTION</span></span>
<span data-ttu-id="d7a9a-106">在指定的環境中建立或更新參照資料集。</span><span class="sxs-lookup"><span data-stu-id="d7a9a-106">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="d7a9a-107">例子</span><span class="sxs-lookup"><span data-stu-id="d7a9a-107">EXAMPLES</span></span>

### <span data-ttu-id="d7a9a-108">範例 1：為指定的環境建立參照資料集</span><span class="sxs-lookup"><span data-stu-id="d7a9a-108">Example 1: Create a reference data set for a specified environment</span></span>  
```powershell
PS C:\> $mykeyproperties = @{ "name" = "device01"; "type" = "Double"}
PS C:\> New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Location eastus -DataStringComparisonBehavior Ordinal -KeyProperty $mykeyproperties

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="d7a9a-109">此命令會為特定環境建立參照資料集。</span><span class="sxs-lookup"><span data-stu-id="d7a9a-109">This command creates a reference data set for a specific environment.</span></span>

## <span data-ttu-id="d7a9a-110">參數</span><span class="sxs-lookup"><span data-stu-id="d7a9a-110">PARAMETERS</span></span>

### <span data-ttu-id="d7a9a-111">-DataStringComparisonBehavior</span><span class="sxs-lookup"><span data-stu-id="d7a9a-111">-DataStringComparisonBehavior</span></span>
<span data-ttu-id="d7a9a-112">您可以使用此屬性設定參照資料集鍵比較行為。</span><span class="sxs-lookup"><span data-stu-id="d7a9a-112">The reference data set key comparison behavior can be set using this property.</span></span>
<span data-ttu-id="d7a9a-113">根據預設，值為 "Ordinal" -這表示在將參照資料與事件聯聯或在新增參照資料時，會執行區分大小寫的金鑰比較。</span><span class="sxs-lookup"><span data-stu-id="d7a9a-113">By default, the value is 'Ordinal' - which means case sensitive key comparison will be performed while joining reference data with events or while adding new reference data.</span></span>
<span data-ttu-id="d7a9a-114">設定好 "OrdinalIgnoreCase" 時，將會使用不區分大小寫的比較。</span><span class="sxs-lookup"><span data-stu-id="d7a9a-114">When 'OrdinalIgnoreCase' is set, case insensitive comparison will be used.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.DataStringComparisonBehavior
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7a9a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7a9a-115">-DefaultProfile</span></span>
<span data-ttu-id="d7a9a-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d7a9a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7a9a-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="d7a9a-117">-EnvironmentName</span></span>
<span data-ttu-id="d7a9a-118">與指定資源群組相關聯的時間序列深入資訊環境名稱。</span><span class="sxs-lookup"><span data-stu-id="d7a9a-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="d7a9a-119">-KeyProperty</span><span class="sxs-lookup"><span data-stu-id="d7a9a-119">-KeyProperty</span></span>
<span data-ttu-id="d7a9a-120">參照資料集的重要屬性清單。</span><span class="sxs-lookup"><span data-stu-id="d7a9a-120">The list of key properties for the reference data set.</span></span>
<span data-ttu-id="d7a9a-121">若要建構，請參閱 KEYPROPERTY 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d7a9a-121">To construct, see NOTES section for KEYPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetKeyProperty[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7a9a-122">-位置</span><span class="sxs-lookup"><span data-stu-id="d7a9a-122">-Location</span></span>
<span data-ttu-id="d7a9a-123">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="d7a9a-123">The location of the resource.</span></span>

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

### <span data-ttu-id="d7a9a-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="d7a9a-124">-Name</span></span>
<span data-ttu-id="d7a9a-125">參照資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7a9a-125">Name of the reference data set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7a9a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7a9a-126">-ResourceGroupName</span></span>
<span data-ttu-id="d7a9a-127">Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7a9a-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="d7a9a-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d7a9a-128">-SubscriptionId</span></span>
<span data-ttu-id="d7a9a-129">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="d7a9a-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="d7a9a-130">-標記</span><span class="sxs-lookup"><span data-stu-id="d7a9a-130">-Tag</span></span>
<span data-ttu-id="d7a9a-131">資源的其他屬性的金鑰值組。</span><span class="sxs-lookup"><span data-stu-id="d7a9a-131">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="d7a9a-132">-確認</span><span class="sxs-lookup"><span data-stu-id="d7a9a-132">-Confirm</span></span>
<span data-ttu-id="d7a9a-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d7a9a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7a9a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7a9a-134">-WhatIf</span></span>
<span data-ttu-id="d7a9a-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d7a9a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7a9a-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d7a9a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7a9a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7a9a-137">CommonParameters</span></span>
<span data-ttu-id="d7a9a-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d7a9a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7a9a-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7a9a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7a9a-140">輸入</span><span class="sxs-lookup"><span data-stu-id="d7a9a-140">INPUTS</span></span>

## <span data-ttu-id="d7a9a-141">輸出</span><span class="sxs-lookup"><span data-stu-id="d7a9a-141">OUTPUTS</span></span>

### <span data-ttu-id="d7a9a-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="d7a9a-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="d7a9a-143">筆記</span><span class="sxs-lookup"><span data-stu-id="d7a9a-143">NOTES</span></span>

<span data-ttu-id="d7a9a-144">別名</span><span class="sxs-lookup"><span data-stu-id="d7a9a-144">ALIASES</span></span>

<span data-ttu-id="d7a9a-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="d7a9a-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d7a9a-146">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d7a9a-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d7a9a-147">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="d7a9a-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d7a9a-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>：參照資料集的重要屬性清單。</span><span class="sxs-lookup"><span data-stu-id="d7a9a-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>: The list of key properties for the reference data set.</span></span>
  - <span data-ttu-id="d7a9a-149">`[Name <String>]`：鍵屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7a9a-149">`[Name <String>]`: The name of the key property.</span></span>
  - <span data-ttu-id="d7a9a-150">`[Type <ReferenceDataKeyPropertyType?>]`：鍵屬性的類型。</span><span class="sxs-lookup"><span data-stu-id="d7a9a-150">`[Type <ReferenceDataKeyPropertyType?>]`: The type of the key property.</span></span>

## <span data-ttu-id="d7a9a-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="d7a9a-151">RELATED LINKS</span></span>

