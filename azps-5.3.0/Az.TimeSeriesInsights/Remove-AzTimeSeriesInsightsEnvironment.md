---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 8b56475d2510099b7873fa444a0dc78497aeb729
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447935"
---
# <span data-ttu-id="ec035-101">Remove-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="ec035-101">Remove-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="ec035-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec035-102">SYNOPSIS</span></span>
<span data-ttu-id="ec035-103">刪除指定訂閱和資源群組中具有指定名稱的環境。</span><span class="sxs-lookup"><span data-stu-id="ec035-103">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="ec035-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec035-104">SYNTAX</span></span>

### <span data-ttu-id="ec035-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="ec035-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ec035-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ec035-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ec035-107">說明</span><span class="sxs-lookup"><span data-stu-id="ec035-107">DESCRIPTION</span></span>
<span data-ttu-id="ec035-108">刪除指定訂閱和資源群組中具有指定名稱的環境。</span><span class="sxs-lookup"><span data-stu-id="ec035-108">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="ec035-109">示例</span><span class="sxs-lookup"><span data-stu-id="ec035-109">EXAMPLES</span></span>

### <span data-ttu-id="ec035-110">範例1：依名稱移除時間序列 insights 環境</span><span class="sxs-lookup"><span data-stu-id="ec035-110">Example 1: Remove a time series insights environment by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill

```

<span data-ttu-id="ec035-111">這個命令會移除時序深入分析環境。</span><span class="sxs-lookup"><span data-stu-id="ec035-111">This command removes a time series insights environment.</span></span>

### <span data-ttu-id="ec035-112">範例2：依物件移除時間序列 insights 環境</span><span class="sxs-lookup"><span data-stu-id="ec035-112">Example 2: Remove a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -InputObject $env

```

<span data-ttu-id="ec035-113">這個命令會移除時序深入分析環境。</span><span class="sxs-lookup"><span data-stu-id="ec035-113">This command removes a time series insights environment.</span></span>

## <span data-ttu-id="ec035-114">參數</span><span class="sxs-lookup"><span data-stu-id="ec035-114">PARAMETERS</span></span>

### <span data-ttu-id="ec035-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec035-115">-DefaultProfile</span></span>
<span data-ttu-id="ec035-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec035-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec035-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec035-117">-InputObject</span></span>
<span data-ttu-id="ec035-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ec035-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec035-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="ec035-119">-Name</span></span>
<span data-ttu-id="ec035-120">與指定的資源群組相關聯之時間序列 Insights 環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec035-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec035-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec035-121">-PassThru</span></span>
<span data-ttu-id="ec035-122">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="ec035-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ec035-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec035-123">-ResourceGroupName</span></span>
<span data-ttu-id="ec035-124">Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec035-124">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec035-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ec035-125">-SubscriptionId</span></span>
<span data-ttu-id="ec035-126">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="ec035-126">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec035-127">-確認</span><span class="sxs-lookup"><span data-stu-id="ec035-127">-Confirm</span></span>
<span data-ttu-id="ec035-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ec035-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec035-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec035-129">-WhatIf</span></span>
<span data-ttu-id="ec035-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ec035-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec035-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ec035-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec035-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec035-132">CommonParameters</span></span>
<span data-ttu-id="ec035-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec035-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec035-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ec035-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec035-135">輸入</span><span class="sxs-lookup"><span data-stu-id="ec035-135">INPUTS</span></span>

### <span data-ttu-id="ec035-136">ITimeSeriesInsightsIdentity （TimeSeriesInsights）的</span><span class="sxs-lookup"><span data-stu-id="ec035-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="ec035-137">輸出</span><span class="sxs-lookup"><span data-stu-id="ec035-137">OUTPUTS</span></span>

### <span data-ttu-id="ec035-138">System.object</span><span class="sxs-lookup"><span data-stu-id="ec035-138">System.Boolean</span></span>

## <span data-ttu-id="ec035-139">筆記</span><span class="sxs-lookup"><span data-stu-id="ec035-139">NOTES</span></span>

<span data-ttu-id="ec035-140">別名</span><span class="sxs-lookup"><span data-stu-id="ec035-140">ALIASES</span></span>

<span data-ttu-id="ec035-141">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="ec035-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ec035-142">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="ec035-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ec035-143">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="ec035-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ec035-144">INPUTOBJECT <ITimeSeriesInsightsIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="ec035-144">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ec035-145">`[AccessPolicyName <String>]`：存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec035-145">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="ec035-146">`[EnvironmentName <String>]`：環境的名稱</span><span class="sxs-lookup"><span data-stu-id="ec035-146">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="ec035-147">`[EventSourceName <String>]`：與指定環境相關聯之時間序列 Insights 事件來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec035-147">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="ec035-148">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="ec035-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ec035-149">`[ReferenceDataSetName <String>]`：參照資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec035-149">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="ec035-150">`[ResourceGroupName <String>]`： Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec035-150">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="ec035-151">`[SubscriptionId <String>]`： Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="ec035-151">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="ec035-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec035-152">RELATED LINKS</span></span>

