---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsplan
schema: 2.0.0
ms.openlocfilehash: 213ae5a86675f6aea43377d298d339a00b37856d
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/22/2020
ms.locfileid: "93966575"
---
# <span data-ttu-id="7204a-101">New-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="7204a-101">New-AzsPlan</span></span>

## <span data-ttu-id="7204a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7204a-102">SYNOPSIS</span></span>
<span data-ttu-id="7204a-103">建立或更新方案。</span><span class="sxs-lookup"><span data-stu-id="7204a-103">Create or update the plan.</span></span>

## <span data-ttu-id="7204a-104">句法</span><span class="sxs-lookup"><span data-stu-id="7204a-104">SYNTAX</span></span>

### <span data-ttu-id="7204a-105">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="7204a-105">CreateExpanded (Default)</span></span>
```
New-AzsPlan -Name <String> -ResourceGroupName <String> -QuotaIds <String[]> [-SubscriptionId <String>]
 [-Description <String>] [-DisplayName <String>] [-ExternalReferenceId <String>] [-Location <String>]
 [-PropertiesName <String>] [-SkuIds <String[]>] [-SubscriptionCount <Int32>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7204a-106">建立</span><span class="sxs-lookup"><span data-stu-id="7204a-106">Create</span></span>
```
New-AzsPlan -Name <String> -ResourceGroupName <String> -PlanDefinition <IPlan> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7204a-107">說明</span><span class="sxs-lookup"><span data-stu-id="7204a-107">DESCRIPTION</span></span>
<span data-ttu-id="7204a-108">建立或更新方案。</span><span class="sxs-lookup"><span data-stu-id="7204a-108">Create or update the plan.</span></span>

## <span data-ttu-id="7204a-109">示例</span><span class="sxs-lookup"><span data-stu-id="7204a-109">EXAMPLES</span></span>

### <span data-ttu-id="7204a-110">範例1</span><span class="sxs-lookup"><span data-stu-id="7204a-110">Example 1</span></span>
```powershell
PS C:\> New-AzsPlan -Name "testplan" -ResourceGroupName "testrg" -QuotaIds "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/locations/redmond/quotas/delegatedProviderQuota" -Description "testplan"

Description         : testplan
DisplayName         : testplan
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan
Location            : redmond
Name                : testplan
PropertiesName      : testplan
QuotaIds            : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/locations/redmond/quotas/delegatedProviderQuota}
SkuIds              : 
SubscriptionCount   : 0
Tags                : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                : Microsoft.Subscriptions.Admin/plans
```

<span data-ttu-id="7204a-111">建立新方案</span><span class="sxs-lookup"><span data-stu-id="7204a-111">Creates a new plan</span></span>

## <span data-ttu-id="7204a-112">參數</span><span class="sxs-lookup"><span data-stu-id="7204a-112">PARAMETERS</span></span>

### <span data-ttu-id="7204a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7204a-113">-DefaultProfile</span></span>
<span data-ttu-id="7204a-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7204a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7204a-115">-描述</span><span class="sxs-lookup"><span data-stu-id="7204a-115">-Description</span></span>
<span data-ttu-id="7204a-116">方案的描述。</span><span class="sxs-lookup"><span data-stu-id="7204a-116">Description of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7204a-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7204a-117">-DisplayName</span></span>
<span data-ttu-id="7204a-118">顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="7204a-118">Display name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7204a-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="7204a-119">-ExternalReferenceId</span></span>
<span data-ttu-id="7204a-120">外部參照識別碼。</span><span class="sxs-lookup"><span data-stu-id="7204a-120">External reference identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7204a-121">-位置</span><span class="sxs-lookup"><span data-stu-id="7204a-121">-Location</span></span>
<span data-ttu-id="7204a-122">資源的位置</span><span class="sxs-lookup"><span data-stu-id="7204a-122">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7204a-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="7204a-123">-Name</span></span>
<span data-ttu-id="7204a-124">方案名稱。</span><span class="sxs-lookup"><span data-stu-id="7204a-124">Name of the plan.</span></span>

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

### <span data-ttu-id="7204a-125">-PlanDefinition</span><span class="sxs-lookup"><span data-stu-id="7204a-125">-PlanDefinition</span></span>
<span data-ttu-id="7204a-126">方案代表提供承租人的配額與功能套件。</span><span class="sxs-lookup"><span data-stu-id="7204a-126">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="7204a-127">租使用者可以透過將其存取權升級為底層雲端服務的優惠來取得此方案。</span><span class="sxs-lookup"><span data-stu-id="7204a-127">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>
<span data-ttu-id="7204a-128">若要建立，請參閱 PLANDEFINITION 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="7204a-128">To construct, see NOTES section for PLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="7204a-129">-PropertiesName</span><span class="sxs-lookup"><span data-stu-id="7204a-129">-PropertiesName</span></span>
<span data-ttu-id="7204a-130">方案名稱。</span><span class="sxs-lookup"><span data-stu-id="7204a-130">Name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7204a-131">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="7204a-131">-QuotaIds</span></span>
<span data-ttu-id="7204a-132">方案中的配額識別碼。</span><span class="sxs-lookup"><span data-stu-id="7204a-132">Quota identifiers under the plan.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7204a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7204a-133">-ResourceGroupName</span></span>
<span data-ttu-id="7204a-134">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="7204a-134">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="7204a-135">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="7204a-135">-SkuIds</span></span>
<span data-ttu-id="7204a-136">SKU 識別碼。</span><span class="sxs-lookup"><span data-stu-id="7204a-136">SKU identifiers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7204a-137">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="7204a-137">-SubscriptionCount</span></span>
<span data-ttu-id="7204a-138">[訂閱計數]。</span><span class="sxs-lookup"><span data-stu-id="7204a-138">Subscription count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7204a-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7204a-139">-SubscriptionId</span></span>
<span data-ttu-id="7204a-140">可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="7204a-140">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7204a-141">-確認</span><span class="sxs-lookup"><span data-stu-id="7204a-141">-Confirm</span></span>
<span data-ttu-id="7204a-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7204a-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7204a-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7204a-143">-WhatIf</span></span>
<span data-ttu-id="7204a-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7204a-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7204a-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7204a-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7204a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7204a-146">CommonParameters</span></span>
<span data-ttu-id="7204a-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7204a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7204a-148">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7204a-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7204a-149">輸入</span><span class="sxs-lookup"><span data-stu-id="7204a-149">INPUTS</span></span>

### <span data-ttu-id="7204a-150">IPlan （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="7204a-150">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

## <span data-ttu-id="7204a-151">輸出</span><span class="sxs-lookup"><span data-stu-id="7204a-151">OUTPUTS</span></span>

### <span data-ttu-id="7204a-152">IPlan （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="7204a-152">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

<span data-ttu-id="7204a-153">別名</span><span class="sxs-lookup"><span data-stu-id="7204a-153">ALIASES</span></span>

## <span data-ttu-id="7204a-154">筆記</span><span class="sxs-lookup"><span data-stu-id="7204a-154">NOTES</span></span>

<span data-ttu-id="7204a-155">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="7204a-155">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7204a-156">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="7204a-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="7204a-157">PLANDEFINITION <IPlan> ：方案代表提供租使用者的配額與功能套件。</span><span class="sxs-lookup"><span data-stu-id="7204a-157">PLANDEFINITION <IPlan>: A plan represents a package of quotas and capabilities that are offered tenants.</span></span> <span data-ttu-id="7204a-158">租使用者可以透過將其存取權升級為底層雲端服務的優惠來取得此方案。</span><span class="sxs-lookup"><span data-stu-id="7204a-158">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>
  - <span data-ttu-id="7204a-159">`[Location <String>]`：資源的位置</span><span class="sxs-lookup"><span data-stu-id="7204a-159">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="7204a-160">`[Description <String>]`：方案的描述。</span><span class="sxs-lookup"><span data-stu-id="7204a-160">`[Description <String>]`: Description of the plan.</span></span>
  - <span data-ttu-id="7204a-161">`[DisplayName <String>]`：顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="7204a-161">`[DisplayName <String>]`: Display name.</span></span>
  - <span data-ttu-id="7204a-162">`[ExternalReferenceId <String>]`：外部參照識別碼。</span><span class="sxs-lookup"><span data-stu-id="7204a-162">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="7204a-163">`[PropertiesName <String>]`：方案名稱。</span><span class="sxs-lookup"><span data-stu-id="7204a-163">`[PropertiesName <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="7204a-164">`[QuotaIds <String[]>]`：方案中的配額識別碼。</span><span class="sxs-lookup"><span data-stu-id="7204a-164">`[QuotaIds <String[]>]`: Quota identifiers under the plan.</span></span>
  - <span data-ttu-id="7204a-165">`[SkuIds <String[]>]`： SKU 識別碼。</span><span class="sxs-lookup"><span data-stu-id="7204a-165">`[SkuIds <String[]>]`: SKU identifiers.</span></span>
  - <span data-ttu-id="7204a-166">`[SubscriptionCount <Int32?>]`：訂閱數。</span><span class="sxs-lookup"><span data-stu-id="7204a-166">`[SubscriptionCount <Int32?>]`: Subscription count.</span></span>

## <span data-ttu-id="7204a-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="7204a-167">RELATED LINKS</span></span>
