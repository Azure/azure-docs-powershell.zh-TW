---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 99271e0933662df4789338bcdcacc5a278fa3b4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912154"
---
# <span data-ttu-id="6b43e-101">Remove-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="6b43e-101">Remove-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="6b43e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6b43e-102">SYNOPSIS</span></span>
<span data-ttu-id="6b43e-103">刪除指定訂閱、資源群組及環境中具有指定名稱的參照資料集</span><span class="sxs-lookup"><span data-stu-id="6b43e-103">Deletes the reference data set with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="6b43e-104">語法</span><span class="sxs-lookup"><span data-stu-id="6b43e-104">SYNTAX</span></span>

### <span data-ttu-id="6b43e-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="6b43e-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6b43e-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6b43e-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6b43e-107">描述</span><span class="sxs-lookup"><span data-stu-id="6b43e-107">DESCRIPTION</span></span>
<span data-ttu-id="6b43e-108">刪除指定訂閱、資源群組及環境中具有指定名稱的參照資料集</span><span class="sxs-lookup"><span data-stu-id="6b43e-108">Deletes the reference data set with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="6b43e-109">例子</span><span class="sxs-lookup"><span data-stu-id="6b43e-109">EXAMPLES</span></span>

### <span data-ttu-id="6b43e-110">範例 1：根據名稱移除指定的參照資料集</span><span class="sxs-lookup"><span data-stu-id="6b43e-110">Example 1: Remove a specified reference data set by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup

```

<span data-ttu-id="6b43e-111">此命令會移除指定的參照資料集。</span><span class="sxs-lookup"><span data-stu-id="6b43e-111">This command removes a specified reference data set.</span></span>

### <span data-ttu-id="6b43e-112">範例 2：移除根據物件指定的參照資料集</span><span class="sxs-lookup"><span data-stu-id="6b43e-112">Example 2: Remove a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

```

<span data-ttu-id="6b43e-113">此命令會移除指定的參照資料集。</span><span class="sxs-lookup"><span data-stu-id="6b43e-113">This command removes a specified reference data set.</span></span>

## <span data-ttu-id="6b43e-114">參數</span><span class="sxs-lookup"><span data-stu-id="6b43e-114">PARAMETERS</span></span>

### <span data-ttu-id="6b43e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b43e-115">-DefaultProfile</span></span>
<span data-ttu-id="6b43e-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6b43e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b43e-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="6b43e-117">-EnvironmentName</span></span>
<span data-ttu-id="6b43e-118">與指定資源群組相關聯的時間序列深入資訊環境名稱。</span><span class="sxs-lookup"><span data-stu-id="6b43e-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="6b43e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b43e-119">-InputObject</span></span>
<span data-ttu-id="6b43e-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6b43e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6b43e-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="6b43e-121">-Name</span></span>
<span data-ttu-id="6b43e-122">時間序列深入資訊參照資料集的名稱與指定環境相關聯。</span><span class="sxs-lookup"><span data-stu-id="6b43e-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b43e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b43e-123">-PassThru</span></span>
<span data-ttu-id="6b43e-124">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="6b43e-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6b43e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b43e-125">-ResourceGroupName</span></span>
<span data-ttu-id="6b43e-126">Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b43e-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="6b43e-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6b43e-127">-SubscriptionId</span></span>
<span data-ttu-id="6b43e-128">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="6b43e-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="6b43e-129">-確認</span><span class="sxs-lookup"><span data-stu-id="6b43e-129">-Confirm</span></span>
<span data-ttu-id="6b43e-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6b43e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b43e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b43e-131">-WhatIf</span></span>
<span data-ttu-id="6b43e-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6b43e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b43e-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6b43e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b43e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b43e-134">CommonParameters</span></span>
<span data-ttu-id="6b43e-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6b43e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b43e-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b43e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b43e-137">輸入</span><span class="sxs-lookup"><span data-stu-id="6b43e-137">INPUTS</span></span>

### <span data-ttu-id="6b43e-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="6b43e-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="6b43e-139">輸出</span><span class="sxs-lookup"><span data-stu-id="6b43e-139">OUTPUTS</span></span>

### <span data-ttu-id="6b43e-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6b43e-140">System.Boolean</span></span>

## <span data-ttu-id="6b43e-141">筆記</span><span class="sxs-lookup"><span data-stu-id="6b43e-141">NOTES</span></span>

<span data-ttu-id="6b43e-142">別名</span><span class="sxs-lookup"><span data-stu-id="6b43e-142">ALIASES</span></span>

<span data-ttu-id="6b43e-143">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="6b43e-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6b43e-144">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6b43e-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6b43e-145">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="6b43e-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6b43e-146">INPUTOBJECT： <ITimeSeriesInsightsIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="6b43e-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6b43e-147">`[AccessPolicyName <String>]`：存取策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b43e-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="6b43e-148">`[EnvironmentName <String>]`：環境名稱</span><span class="sxs-lookup"><span data-stu-id="6b43e-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="6b43e-149">`[EventSourceName <String>]`：與指定環境相關聯的時間序列深入資訊事件來源名稱。</span><span class="sxs-lookup"><span data-stu-id="6b43e-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="6b43e-150">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="6b43e-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6b43e-151">`[ReferenceDataSetName <String>]`：參照資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b43e-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="6b43e-152">`[ResourceGroupName <String>]`：Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b43e-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="6b43e-153">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="6b43e-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="6b43e-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="6b43e-154">RELATED LINKS</span></span>

