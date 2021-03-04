---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: 3ef56e9c554b7efbd762b4b373806aad649e0449
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910894"
---
# <span data-ttu-id="b9f78-101">Update-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b9f78-101">Update-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="b9f78-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b9f78-102">SYNOPSIS</span></span>
<span data-ttu-id="b9f78-103">使用指定訂閱、資源群組及環境中的指定名稱更新存取策略。</span><span class="sxs-lookup"><span data-stu-id="b9f78-103">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="b9f78-104">語法</span><span class="sxs-lookup"><span data-stu-id="b9f78-104">SYNTAX</span></span>

### <span data-ttu-id="b9f78-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="b9f78-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b9f78-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b9f78-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-Description <String>]
 [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b9f78-107">描述</span><span class="sxs-lookup"><span data-stu-id="b9f78-107">DESCRIPTION</span></span>
<span data-ttu-id="b9f78-108">使用指定訂閱、資源群組及環境中的指定名稱更新存取策略。</span><span class="sxs-lookup"><span data-stu-id="b9f78-108">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="b9f78-109">例子</span><span class="sxs-lookup"><span data-stu-id="b9f78-109">EXAMPLES</span></span>

### <span data-ttu-id="b9f78-110">範例 1：根據名稱更新指定的存取策略</span><span class="sxs-lookup"><span data-stu-id="b9f78-110">Example 1: Update a specified access policy by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup -Role Contributor,Reader

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="b9f78-111">此命令會更新指定的存取策略。</span><span class="sxs-lookup"><span data-stu-id="b9f78-111">This command updates a specified access policy.</span></span>

### <span data-ttu-id="b9f78-112">範例 2：根據物件更新指定的存取策略</span><span class="sxs-lookup"><span data-stu-id="b9f78-112">Example 2: Update a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -InputObject $policy -Role Contributor

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="b9f78-113">此命令會更新指定的存取策略。</span><span class="sxs-lookup"><span data-stu-id="b9f78-113">This command updates a specified access policy.</span></span>

## <span data-ttu-id="b9f78-114">參數</span><span class="sxs-lookup"><span data-stu-id="b9f78-114">PARAMETERS</span></span>

### <span data-ttu-id="b9f78-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9f78-115">-DefaultProfile</span></span>
<span data-ttu-id="b9f78-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b9f78-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9f78-117">-描述</span><span class="sxs-lookup"><span data-stu-id="b9f78-117">-Description</span></span>
<span data-ttu-id="b9f78-118">存取策略的描述。</span><span class="sxs-lookup"><span data-stu-id="b9f78-118">An description of the access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f78-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="b9f78-119">-EnvironmentName</span></span>
<span data-ttu-id="b9f78-120">與指定資源群組相關聯的時間序列深入資訊環境名稱。</span><span class="sxs-lookup"><span data-stu-id="b9f78-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="b9f78-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9f78-121">-InputObject</span></span>
<span data-ttu-id="b9f78-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b9f78-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b9f78-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="b9f78-123">-Name</span></span>
<span data-ttu-id="b9f78-124">與指定環境相關聯的時間系列深入資訊存取策略名稱。</span><span class="sxs-lookup"><span data-stu-id="b9f78-124">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f78-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9f78-125">-ResourceGroupName</span></span>
<span data-ttu-id="b9f78-126">Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b9f78-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="b9f78-127">-角色</span><span class="sxs-lookup"><span data-stu-id="b9f78-127">-Role</span></span>
<span data-ttu-id="b9f78-128">主體在環境中指派的角色清單。</span><span class="sxs-lookup"><span data-stu-id="b9f78-128">The list of roles the principal is assigned on the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.AccessPolicyRole[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f78-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b9f78-129">-SubscriptionId</span></span>
<span data-ttu-id="b9f78-130">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="b9f78-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="b9f78-131">-確認</span><span class="sxs-lookup"><span data-stu-id="b9f78-131">-Confirm</span></span>
<span data-ttu-id="b9f78-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b9f78-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9f78-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9f78-133">-WhatIf</span></span>
<span data-ttu-id="b9f78-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b9f78-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9f78-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b9f78-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9f78-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9f78-136">CommonParameters</span></span>
<span data-ttu-id="b9f78-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b9f78-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9f78-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9f78-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9f78-139">輸入</span><span class="sxs-lookup"><span data-stu-id="b9f78-139">INPUTS</span></span>

### <span data-ttu-id="b9f78-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="b9f78-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="b9f78-141">輸出</span><span class="sxs-lookup"><span data-stu-id="b9f78-141">OUTPUTS</span></span>

### <span data-ttu-id="b9f78-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="b9f78-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="b9f78-143">筆記</span><span class="sxs-lookup"><span data-stu-id="b9f78-143">NOTES</span></span>

<span data-ttu-id="b9f78-144">別名</span><span class="sxs-lookup"><span data-stu-id="b9f78-144">ALIASES</span></span>

<span data-ttu-id="b9f78-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b9f78-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b9f78-146">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b9f78-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b9f78-147">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b9f78-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b9f78-148">INPUTOBJECT： <ITimeSeriesInsightsIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b9f78-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b9f78-149">`[AccessPolicyName <String>]`：存取策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="b9f78-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="b9f78-150">`[EnvironmentName <String>]`：環境名稱</span><span class="sxs-lookup"><span data-stu-id="b9f78-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="b9f78-151">`[EventSourceName <String>]`：與指定環境相關聯的時間序列深入資訊事件來源名稱。</span><span class="sxs-lookup"><span data-stu-id="b9f78-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="b9f78-152">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="b9f78-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b9f78-153">`[ReferenceDataSetName <String>]`：參照資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="b9f78-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="b9f78-154">`[ResourceGroupName <String>]`：Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b9f78-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="b9f78-155">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="b9f78-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="b9f78-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="b9f78-156">RELATED LINKS</span></span>

