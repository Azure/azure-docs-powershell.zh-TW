---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 89fa39a5e6e1bb2ded61c41dd553b6d7d0473d4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904766"
---
# <span data-ttu-id="1c310-101">Remove-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="1c310-101">Remove-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="1c310-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1c310-102">SYNOPSIS</span></span>
<span data-ttu-id="1c310-103">刪除指定訂閱和資源群組中具有指定名稱的環境。</span><span class="sxs-lookup"><span data-stu-id="1c310-103">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="1c310-104">語法</span><span class="sxs-lookup"><span data-stu-id="1c310-104">SYNTAX</span></span>

### <span data-ttu-id="1c310-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="1c310-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1c310-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1c310-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1c310-107">描述</span><span class="sxs-lookup"><span data-stu-id="1c310-107">DESCRIPTION</span></span>
<span data-ttu-id="1c310-108">刪除指定訂閱和資源群組中具有指定名稱的環境。</span><span class="sxs-lookup"><span data-stu-id="1c310-108">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="1c310-109">例子</span><span class="sxs-lookup"><span data-stu-id="1c310-109">EXAMPLES</span></span>

### <span data-ttu-id="1c310-110">範例 1：根據名稱移除時間序列深入資訊環境</span><span class="sxs-lookup"><span data-stu-id="1c310-110">Example 1: Remove a time series insights environment by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill

```

<span data-ttu-id="1c310-111">此命令會移除時間序列深入資訊環境。</span><span class="sxs-lookup"><span data-stu-id="1c310-111">This command removes a time series insights environment.</span></span>

### <span data-ttu-id="1c310-112">範例 2：根據物件移除時間序列深入資訊環境</span><span class="sxs-lookup"><span data-stu-id="1c310-112">Example 2: Remove a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -InputObject $env

```

<span data-ttu-id="1c310-113">此命令會移除時間序列深入資訊環境。</span><span class="sxs-lookup"><span data-stu-id="1c310-113">This command removes a time series insights environment.</span></span>

## <span data-ttu-id="1c310-114">參數</span><span class="sxs-lookup"><span data-stu-id="1c310-114">PARAMETERS</span></span>

### <span data-ttu-id="1c310-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c310-115">-DefaultProfile</span></span>
<span data-ttu-id="1c310-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1c310-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c310-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c310-117">-InputObject</span></span>
<span data-ttu-id="1c310-118">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="1c310-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1c310-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="1c310-119">-Name</span></span>
<span data-ttu-id="1c310-120">與指定資源群組相關聯的時間序列深入資訊環境名稱。</span><span class="sxs-lookup"><span data-stu-id="1c310-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="1c310-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c310-121">-PassThru</span></span>
<span data-ttu-id="1c310-122">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="1c310-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1c310-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c310-123">-ResourceGroupName</span></span>
<span data-ttu-id="1c310-124">Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c310-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="1c310-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1c310-125">-SubscriptionId</span></span>
<span data-ttu-id="1c310-126">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="1c310-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="1c310-127">-確認</span><span class="sxs-lookup"><span data-stu-id="1c310-127">-Confirm</span></span>
<span data-ttu-id="1c310-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1c310-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c310-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c310-129">-WhatIf</span></span>
<span data-ttu-id="1c310-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1c310-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c310-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1c310-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c310-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c310-132">CommonParameters</span></span>
<span data-ttu-id="1c310-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1c310-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c310-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c310-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c310-135">輸入</span><span class="sxs-lookup"><span data-stu-id="1c310-135">INPUTS</span></span>

### <span data-ttu-id="1c310-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="1c310-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="1c310-137">輸出</span><span class="sxs-lookup"><span data-stu-id="1c310-137">OUTPUTS</span></span>

### <span data-ttu-id="1c310-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1c310-138">System.Boolean</span></span>

## <span data-ttu-id="1c310-139">筆記</span><span class="sxs-lookup"><span data-stu-id="1c310-139">NOTES</span></span>

<span data-ttu-id="1c310-140">別名</span><span class="sxs-lookup"><span data-stu-id="1c310-140">ALIASES</span></span>

<span data-ttu-id="1c310-141">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="1c310-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1c310-142">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="1c310-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1c310-143">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="1c310-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1c310-144">INPUTOBJECT： <ITimeSeriesInsightsIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="1c310-144">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1c310-145">`[AccessPolicyName <String>]`：存取策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c310-145">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="1c310-146">`[EnvironmentName <String>]`：環境名稱</span><span class="sxs-lookup"><span data-stu-id="1c310-146">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="1c310-147">`[EventSourceName <String>]`：與指定環境相關聯的時間序列深入資訊事件來源名稱。</span><span class="sxs-lookup"><span data-stu-id="1c310-147">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="1c310-148">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="1c310-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1c310-149">`[ReferenceDataSetName <String>]`：參照資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c310-149">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="1c310-150">`[ResourceGroupName <String>]`：Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c310-150">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="1c310-151">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="1c310-151">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="1c310-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c310-152">RELATED LINKS</span></span>

