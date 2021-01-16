---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: e776b0e11fedd0b2903135b9b640c3b704706027
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275784"
---
# <span data-ttu-id="bd857-101">Update-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bd857-101">Update-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="bd857-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bd857-102">SYNOPSIS</span></span>
<span data-ttu-id="bd857-103">在指定的訂閱、資源群組和環境中，以指定的名稱更新存取原則。</span><span class="sxs-lookup"><span data-stu-id="bd857-103">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="bd857-104">句法</span><span class="sxs-lookup"><span data-stu-id="bd857-104">SYNTAX</span></span>

### <span data-ttu-id="bd857-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="bd857-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bd857-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="bd857-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-Description <String>]
 [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bd857-107">說明</span><span class="sxs-lookup"><span data-stu-id="bd857-107">DESCRIPTION</span></span>
<span data-ttu-id="bd857-108">在指定的訂閱、資源群組和環境中，以指定的名稱更新存取原則。</span><span class="sxs-lookup"><span data-stu-id="bd857-108">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="bd857-109">示例</span><span class="sxs-lookup"><span data-stu-id="bd857-109">EXAMPLES</span></span>

### <span data-ttu-id="bd857-110">範例1：依名稱更新指定的存取原則</span><span class="sxs-lookup"><span data-stu-id="bd857-110">Example 1: Update a specified access policy by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup -Role Contributor,Reader

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="bd857-111">這個命令會更新指定的存取原則。</span><span class="sxs-lookup"><span data-stu-id="bd857-111">This command updates a specified access policy.</span></span>

### <span data-ttu-id="bd857-112">範例2：依物件更新指定的存取原則</span><span class="sxs-lookup"><span data-stu-id="bd857-112">Example 2: Update a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -InputObject $policy -Role Contributor

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="bd857-113">這個命令會更新指定的存取原則。</span><span class="sxs-lookup"><span data-stu-id="bd857-113">This command updates a specified access policy.</span></span>

## <span data-ttu-id="bd857-114">參數</span><span class="sxs-lookup"><span data-stu-id="bd857-114">PARAMETERS</span></span>

### <span data-ttu-id="bd857-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd857-115">-DefaultProfile</span></span>
<span data-ttu-id="bd857-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bd857-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd857-117">-描述</span><span class="sxs-lookup"><span data-stu-id="bd857-117">-Description</span></span>
<span data-ttu-id="bd857-118">存取原則的描述。</span><span class="sxs-lookup"><span data-stu-id="bd857-118">An description of the access policy.</span></span>

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

### <span data-ttu-id="bd857-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="bd857-119">-EnvironmentName</span></span>
<span data-ttu-id="bd857-120">與指定的資源群組相關聯之時間序列 Insights 環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd857-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="bd857-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd857-121">-InputObject</span></span>
<span data-ttu-id="bd857-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="bd857-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bd857-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="bd857-123">-Name</span></span>
<span data-ttu-id="bd857-124">與指定環境相關聯之時間序列 Insights 存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd857-124">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

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

### <span data-ttu-id="bd857-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd857-125">-ResourceGroupName</span></span>
<span data-ttu-id="bd857-126">Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd857-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="bd857-127">-角色</span><span class="sxs-lookup"><span data-stu-id="bd857-127">-Role</span></span>
<span data-ttu-id="bd857-128">在環境中指派主體的角色清單。</span><span class="sxs-lookup"><span data-stu-id="bd857-128">The list of roles the principal is assigned on the environment.</span></span>

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

### <span data-ttu-id="bd857-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bd857-129">-SubscriptionId</span></span>
<span data-ttu-id="bd857-130">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="bd857-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="bd857-131">-確認</span><span class="sxs-lookup"><span data-stu-id="bd857-131">-Confirm</span></span>
<span data-ttu-id="bd857-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bd857-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd857-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd857-133">-WhatIf</span></span>
<span data-ttu-id="bd857-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bd857-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd857-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bd857-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd857-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd857-136">CommonParameters</span></span>
<span data-ttu-id="bd857-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bd857-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd857-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bd857-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd857-139">輸入</span><span class="sxs-lookup"><span data-stu-id="bd857-139">INPUTS</span></span>

### <span data-ttu-id="bd857-140">ITimeSeriesInsightsIdentity （TimeSeriesInsights）的</span><span class="sxs-lookup"><span data-stu-id="bd857-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="bd857-141">輸出</span><span class="sxs-lookup"><span data-stu-id="bd857-141">OUTPUTS</span></span>

### <span data-ttu-id="bd857-142">IAccessPolicyResource （TimeSeriesInsights）。 Api20200515。</span><span class="sxs-lookup"><span data-stu-id="bd857-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="bd857-143">筆記</span><span class="sxs-lookup"><span data-stu-id="bd857-143">NOTES</span></span>

<span data-ttu-id="bd857-144">別名</span><span class="sxs-lookup"><span data-stu-id="bd857-144">ALIASES</span></span>

<span data-ttu-id="bd857-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="bd857-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bd857-146">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="bd857-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bd857-147">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="bd857-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bd857-148">INPUTOBJECT <ITimeSeriesInsightsIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="bd857-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bd857-149">`[AccessPolicyName <String>]`：存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd857-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="bd857-150">`[EnvironmentName <String>]`：環境的名稱</span><span class="sxs-lookup"><span data-stu-id="bd857-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="bd857-151">`[EventSourceName <String>]`：與指定環境相關聯之時間序列 Insights 事件來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd857-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="bd857-152">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="bd857-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bd857-153">`[ReferenceDataSetName <String>]`：參照資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd857-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="bd857-154">`[ResourceGroupName <String>]`： Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd857-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="bd857-155">`[SubscriptionId <String>]`： Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="bd857-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="bd857-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd857-156">RELATED LINKS</span></span>

