---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: 2fe9a418f135471e18f469bf0dcf5ce515de1c2e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904774"
---
# <span data-ttu-id="28c58-101">Remove-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="28c58-101">Remove-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="28c58-102">簡介</span><span class="sxs-lookup"><span data-stu-id="28c58-102">SYNOPSIS</span></span>
<span data-ttu-id="28c58-103">刪除指定訂閱、資源群組及環境中具有指定名稱的存取策略</span><span class="sxs-lookup"><span data-stu-id="28c58-103">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="28c58-104">語法</span><span class="sxs-lookup"><span data-stu-id="28c58-104">SYNTAX</span></span>

### <span data-ttu-id="28c58-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="28c58-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="28c58-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="28c58-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="28c58-107">描述</span><span class="sxs-lookup"><span data-stu-id="28c58-107">DESCRIPTION</span></span>
<span data-ttu-id="28c58-108">刪除指定訂閱、資源群組及環境中具有指定名稱的存取策略</span><span class="sxs-lookup"><span data-stu-id="28c58-108">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="28c58-109">例子</span><span class="sxs-lookup"><span data-stu-id="28c58-109">EXAMPLES</span></span>

### <span data-ttu-id="28c58-110">範例 1：根據名稱移除指定的存取策略</span><span class="sxs-lookup"><span data-stu-id="28c58-110">Example 1: Remove a specified access policy by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup

```

<span data-ttu-id="28c58-111">此命令會移除指定的存取策略。</span><span class="sxs-lookup"><span data-stu-id="28c58-111">This command removes a specified access policy.</span></span>

### <span data-ttu-id="28c58-112">範例 2：根據物件移除指定的存取策略</span><span class="sxs-lookup"><span data-stu-id="28c58-112">Example 2: Remove a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -InputObject $policy

```

<span data-ttu-id="28c58-113">此命令會移除指定的存取策略。</span><span class="sxs-lookup"><span data-stu-id="28c58-113">This command removes a specified access policy.</span></span>

## <span data-ttu-id="28c58-114">參數</span><span class="sxs-lookup"><span data-stu-id="28c58-114">PARAMETERS</span></span>

### <span data-ttu-id="28c58-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28c58-115">-DefaultProfile</span></span>
<span data-ttu-id="28c58-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="28c58-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28c58-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="28c58-117">-EnvironmentName</span></span>
<span data-ttu-id="28c58-118">與指定資源群組相關聯的時間序列深入資訊環境名稱。</span><span class="sxs-lookup"><span data-stu-id="28c58-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="28c58-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28c58-119">-InputObject</span></span>
<span data-ttu-id="28c58-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="28c58-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="28c58-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="28c58-121">-Name</span></span>
<span data-ttu-id="28c58-122">與指定環境相關聯的時間系列深入資訊存取策略名稱。</span><span class="sxs-lookup"><span data-stu-id="28c58-122">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28c58-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28c58-123">-PassThru</span></span>
<span data-ttu-id="28c58-124">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="28c58-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="28c58-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28c58-125">-ResourceGroupName</span></span>
<span data-ttu-id="28c58-126">Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="28c58-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="28c58-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="28c58-127">-SubscriptionId</span></span>
<span data-ttu-id="28c58-128">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="28c58-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="28c58-129">-確認</span><span class="sxs-lookup"><span data-stu-id="28c58-129">-Confirm</span></span>
<span data-ttu-id="28c58-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="28c58-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28c58-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28c58-131">-WhatIf</span></span>
<span data-ttu-id="28c58-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="28c58-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28c58-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28c58-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28c58-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28c58-134">CommonParameters</span></span>
<span data-ttu-id="28c58-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="28c58-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28c58-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28c58-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28c58-137">輸入</span><span class="sxs-lookup"><span data-stu-id="28c58-137">INPUTS</span></span>

### <span data-ttu-id="28c58-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="28c58-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="28c58-139">輸出</span><span class="sxs-lookup"><span data-stu-id="28c58-139">OUTPUTS</span></span>

### <span data-ttu-id="28c58-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="28c58-140">System.Boolean</span></span>

## <span data-ttu-id="28c58-141">筆記</span><span class="sxs-lookup"><span data-stu-id="28c58-141">NOTES</span></span>

<span data-ttu-id="28c58-142">別名</span><span class="sxs-lookup"><span data-stu-id="28c58-142">ALIASES</span></span>

<span data-ttu-id="28c58-143">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="28c58-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="28c58-144">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="28c58-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="28c58-145">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="28c58-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="28c58-146">INPUTOBJECT： <ITimeSeriesInsightsIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="28c58-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="28c58-147">`[AccessPolicyName <String>]`：存取策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="28c58-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="28c58-148">`[EnvironmentName <String>]`：環境名稱</span><span class="sxs-lookup"><span data-stu-id="28c58-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="28c58-149">`[EventSourceName <String>]`：與指定環境相關聯的時間序列深入資訊事件來源名稱。</span><span class="sxs-lookup"><span data-stu-id="28c58-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="28c58-150">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="28c58-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="28c58-151">`[ReferenceDataSetName <String>]`：參照資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="28c58-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="28c58-152">`[ResourceGroupName <String>]`：Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="28c58-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="28c58-153">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="28c58-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="28c58-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="28c58-154">RELATED LINKS</span></span>

