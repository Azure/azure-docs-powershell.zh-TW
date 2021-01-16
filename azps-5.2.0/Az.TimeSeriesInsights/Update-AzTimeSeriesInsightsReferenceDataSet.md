---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 7dbced00ee2e39c536765bd16a19fbe7a66e291b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279473"
---
# <span data-ttu-id="55a50-101">Update-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="55a50-101">Update-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="55a50-102">摘要</span><span class="sxs-lookup"><span data-stu-id="55a50-102">SYNOPSIS</span></span>
<span data-ttu-id="55a50-103">在指定的訂閱、資源群組和環境中，以指定的名稱更新參照資料集。</span><span class="sxs-lookup"><span data-stu-id="55a50-103">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="55a50-104">句法</span><span class="sxs-lookup"><span data-stu-id="55a50-104">SYNTAX</span></span>

### <span data-ttu-id="55a50-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="55a50-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="55a50-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="55a50-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="55a50-107">說明</span><span class="sxs-lookup"><span data-stu-id="55a50-107">DESCRIPTION</span></span>
<span data-ttu-id="55a50-108">在指定的訂閱、資源群組和環境中，以指定的名稱更新參照資料集。</span><span class="sxs-lookup"><span data-stu-id="55a50-108">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="55a50-109">示例</span><span class="sxs-lookup"><span data-stu-id="55a50-109">EXAMPLES</span></span>

### <span data-ttu-id="55a50-110">範例1：依名稱更新指定的參照資料集</span><span class="sxs-lookup"><span data-stu-id="55a50-110">Example 1: Update a specified reference data set by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="55a50-111">這個命令會更新指定的參照資料集。</span><span class="sxs-lookup"><span data-stu-id="55a50-111">This command updates a specified reference data set.</span></span>

### <span data-ttu-id="55a50-112">範例2：更新依物件設定的指定參照資料</span><span class="sxs-lookup"><span data-stu-id="55a50-112">Example 2: Update a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="55a50-113">這個命令會更新指定的參照資料集。</span><span class="sxs-lookup"><span data-stu-id="55a50-113">This command updates a specified reference data set.</span></span>

## <span data-ttu-id="55a50-114">參數</span><span class="sxs-lookup"><span data-stu-id="55a50-114">PARAMETERS</span></span>

### <span data-ttu-id="55a50-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55a50-115">-DefaultProfile</span></span>
<span data-ttu-id="55a50-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="55a50-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55a50-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="55a50-117">-EnvironmentName</span></span>
<span data-ttu-id="55a50-118">與指定的資源群組相關聯之時間序列 Insights 環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="55a50-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="55a50-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55a50-119">-InputObject</span></span>
<span data-ttu-id="55a50-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="55a50-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="55a50-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="55a50-121">-Name</span></span>
<span data-ttu-id="55a50-122">與指定環境關聯的時間序列 Insights 參考資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="55a50-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55a50-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55a50-123">-ResourceGroupName</span></span>
<span data-ttu-id="55a50-124">Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="55a50-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="55a50-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="55a50-125">-SubscriptionId</span></span>
<span data-ttu-id="55a50-126">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="55a50-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="55a50-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="55a50-127">-Tag</span></span>
<span data-ttu-id="55a50-128">參照資料集之其他屬性的鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="55a50-128">Key-value pairs of additional properties for the reference data set.</span></span>

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

### <span data-ttu-id="55a50-129">-確認</span><span class="sxs-lookup"><span data-stu-id="55a50-129">-Confirm</span></span>
<span data-ttu-id="55a50-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="55a50-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55a50-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55a50-131">-WhatIf</span></span>
<span data-ttu-id="55a50-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="55a50-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55a50-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55a50-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55a50-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55a50-134">CommonParameters</span></span>
<span data-ttu-id="55a50-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="55a50-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55a50-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="55a50-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55a50-137">輸入</span><span class="sxs-lookup"><span data-stu-id="55a50-137">INPUTS</span></span>

### <span data-ttu-id="55a50-138">ITimeSeriesInsightsIdentity （TimeSeriesInsights）的</span><span class="sxs-lookup"><span data-stu-id="55a50-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="55a50-139">輸出</span><span class="sxs-lookup"><span data-stu-id="55a50-139">OUTPUTS</span></span>

### <span data-ttu-id="55a50-140">IReferenceDataSetResource （TimeSeriesInsights）。 Api20200515。</span><span class="sxs-lookup"><span data-stu-id="55a50-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="55a50-141">筆記</span><span class="sxs-lookup"><span data-stu-id="55a50-141">NOTES</span></span>

<span data-ttu-id="55a50-142">別名</span><span class="sxs-lookup"><span data-stu-id="55a50-142">ALIASES</span></span>

<span data-ttu-id="55a50-143">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="55a50-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="55a50-144">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="55a50-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="55a50-145">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="55a50-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="55a50-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="55a50-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="55a50-147">`[AccessPolicyName <String>]`：存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="55a50-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="55a50-148">`[EnvironmentName <String>]`：環境的名稱</span><span class="sxs-lookup"><span data-stu-id="55a50-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="55a50-149">`[EventSourceName <String>]`：與指定環境相關聯之時間序列 Insights 事件來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="55a50-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="55a50-150">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="55a50-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="55a50-151">`[ReferenceDataSetName <String>]`：參照資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="55a50-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="55a50-152">`[ResourceGroupName <String>]`： Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="55a50-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="55a50-153">`[SubscriptionId <String>]`： Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="55a50-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="55a50-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="55a50-154">RELATED LINKS</span></span>

