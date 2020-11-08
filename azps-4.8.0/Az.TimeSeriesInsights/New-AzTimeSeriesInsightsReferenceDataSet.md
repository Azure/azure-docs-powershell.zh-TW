---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 39bbdf61a5068ea32f1febf66249213264235dfc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129093"
---
# <span data-ttu-id="ffed0-101">New-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="ffed0-101">New-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="ffed0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ffed0-102">SYNOPSIS</span></span>
<span data-ttu-id="ffed0-103">在指定的環境中建立或更新參照資料集。</span><span class="sxs-lookup"><span data-stu-id="ffed0-103">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="ffed0-104">句法</span><span class="sxs-lookup"><span data-stu-id="ffed0-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -KeyProperty <IReferenceDataSetKeyProperty[]> -Location <String> [-SubscriptionId <String>]
 [-DataStringComparisonBehavior <DataStringComparisonBehavior>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ffed0-105">說明</span><span class="sxs-lookup"><span data-stu-id="ffed0-105">DESCRIPTION</span></span>
<span data-ttu-id="ffed0-106">在指定的環境中建立或更新參照資料集。</span><span class="sxs-lookup"><span data-stu-id="ffed0-106">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="ffed0-107">示例</span><span class="sxs-lookup"><span data-stu-id="ffed0-107">EXAMPLES</span></span>

### <span data-ttu-id="ffed0-108">範例1：建立指定環境的參照資料集</span><span class="sxs-lookup"><span data-stu-id="ffed0-108">Example 1: Create a reference data set for a specified environment</span></span>  
```powershell
PS C:\> $mykeyproperties = @{ "name" = "device01"; "type" = "Double"}
PS C:\> New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Location eastus -DataStringComparisonBehavior Ordinal -KeyProperty $mykeyproperties

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="ffed0-109">這個命令會針對特定環境建立參照資料集。</span><span class="sxs-lookup"><span data-stu-id="ffed0-109">This command creates a reference data set for a specific environment.</span></span>

## <span data-ttu-id="ffed0-110">參數</span><span class="sxs-lookup"><span data-stu-id="ffed0-110">PARAMETERS</span></span>

### <span data-ttu-id="ffed0-111">-DataStringComparisonBehavior</span><span class="sxs-lookup"><span data-stu-id="ffed0-111">-DataStringComparisonBehavior</span></span>
<span data-ttu-id="ffed0-112">參照資料集金鑰比較行為可以使用這個屬性來設定。</span><span class="sxs-lookup"><span data-stu-id="ffed0-112">The reference data set key comparison behavior can be set using this property.</span></span>
<span data-ttu-id="ffed0-113">根據預設，此值是 "Ordinal"，這表示在使用事件或新增參照資料加入參考資料時，會執行大小寫區分的金鑰比較。</span><span class="sxs-lookup"><span data-stu-id="ffed0-113">By default, the value is 'Ordinal' - which means case sensitive key comparison will be performed while joining reference data with events or while adding new reference data.</span></span>
<span data-ttu-id="ffed0-114">設定 ' OrdinalIgnoreCase」時，將會使用不區分大小寫的比較。</span><span class="sxs-lookup"><span data-stu-id="ffed0-114">When 'OrdinalIgnoreCase' is set, case insensitive comparison will be used.</span></span>

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

### <span data-ttu-id="ffed0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffed0-115">-DefaultProfile</span></span>
<span data-ttu-id="ffed0-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ffed0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffed0-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="ffed0-117">-EnvironmentName</span></span>
<span data-ttu-id="ffed0-118">與指定的資源群組相關聯之時間序列 Insights 環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="ffed0-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="ffed0-119">-KeyProperty</span><span class="sxs-lookup"><span data-stu-id="ffed0-119">-KeyProperty</span></span>
<span data-ttu-id="ffed0-120">參照資料集的主要屬性清單。</span><span class="sxs-lookup"><span data-stu-id="ffed0-120">The list of key properties for the reference data set.</span></span>
<span data-ttu-id="ffed0-121">若要建立，請參閱 KEYPROPERTY 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="ffed0-121">To construct, see NOTES section for KEYPROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="ffed0-122">-位置</span><span class="sxs-lookup"><span data-stu-id="ffed0-122">-Location</span></span>
<span data-ttu-id="ffed0-123">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="ffed0-123">The location of the resource.</span></span>

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

### <span data-ttu-id="ffed0-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="ffed0-124">-Name</span></span>
<span data-ttu-id="ffed0-125">參照資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="ffed0-125">Name of the reference data set.</span></span>

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

### <span data-ttu-id="ffed0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffed0-126">-ResourceGroupName</span></span>
<span data-ttu-id="ffed0-127">Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ffed0-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="ffed0-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ffed0-128">-SubscriptionId</span></span>
<span data-ttu-id="ffed0-129">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="ffed0-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="ffed0-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="ffed0-130">-Tag</span></span>
<span data-ttu-id="ffed0-131">資源之其他屬性的鍵值對。</span><span class="sxs-lookup"><span data-stu-id="ffed0-131">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="ffed0-132">-確認</span><span class="sxs-lookup"><span data-stu-id="ffed0-132">-Confirm</span></span>
<span data-ttu-id="ffed0-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ffed0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffed0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffed0-134">-WhatIf</span></span>
<span data-ttu-id="ffed0-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ffed0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffed0-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ffed0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffed0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffed0-137">CommonParameters</span></span>
<span data-ttu-id="ffed0-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ffed0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffed0-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ffed0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffed0-140">輸入</span><span class="sxs-lookup"><span data-stu-id="ffed0-140">INPUTS</span></span>

## <span data-ttu-id="ffed0-141">輸出</span><span class="sxs-lookup"><span data-stu-id="ffed0-141">OUTPUTS</span></span>

### <span data-ttu-id="ffed0-142">IReferenceDataSetResource （TimeSeriesInsights）。 Api20200515。</span><span class="sxs-lookup"><span data-stu-id="ffed0-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="ffed0-143">筆記</span><span class="sxs-lookup"><span data-stu-id="ffed0-143">NOTES</span></span>

<span data-ttu-id="ffed0-144">別名</span><span class="sxs-lookup"><span data-stu-id="ffed0-144">ALIASES</span></span>

<span data-ttu-id="ffed0-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="ffed0-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ffed0-146">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="ffed0-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ffed0-147">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="ffed0-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ffed0-148">KEYPROPERTY <IReferenceDataSetKeyProperty [] >：參照資料集的主要屬性清單。</span><span class="sxs-lookup"><span data-stu-id="ffed0-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>: The list of key properties for the reference data set.</span></span>
  - <span data-ttu-id="ffed0-149">`[Name <String>]`：主要屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="ffed0-149">`[Name <String>]`: The name of the key property.</span></span>
  - <span data-ttu-id="ffed0-150">`[Type <ReferenceDataKeyPropertyType?>]`：主要屬性的類型。</span><span class="sxs-lookup"><span data-stu-id="ffed0-150">`[Type <ReferenceDataKeyPropertyType?>]`: The type of the key property.</span></span>

## <span data-ttu-id="ffed0-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="ffed0-151">RELATED LINKS</span></span>

