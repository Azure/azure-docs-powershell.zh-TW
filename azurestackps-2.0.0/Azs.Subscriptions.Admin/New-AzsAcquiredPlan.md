---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: 0db0f7ae4358e49ff62f94132701be1f4bd4d0b7
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/22/2020
ms.locfileid: "93966592"
---
# <span data-ttu-id="acf1d-101">New-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="acf1d-101">New-AzsAcquiredPlan</span></span>

## <span data-ttu-id="acf1d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="acf1d-102">SYNOPSIS</span></span>


## <span data-ttu-id="acf1d-103">句法</span><span class="sxs-lookup"><span data-stu-id="acf1d-103">SYNTAX</span></span>

### <span data-ttu-id="acf1d-104">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="acf1d-104">CreateExpanded (Default)</span></span>
```
New-AzsAcquiredPlan -TargetSubscriptionId <String> [-PlanAcquisitionId <String>] [-SubscriptionId <String>]
 [-AcquisitionTime <DateTime>] [-ExternalReferenceId <String>] [-Id <String>] [-PlanId <String>]
 [-ProvisioningState <ProvisioningState>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="acf1d-105">建立</span><span class="sxs-lookup"><span data-stu-id="acf1d-105">Create</span></span>
```
New-AzsAcquiredPlan -TargetSubscriptionId <String> -AcquiredPlanDefinition <IPlanAcquisition>
 [-PlanAcquisitionId <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="acf1d-106">說明</span><span class="sxs-lookup"><span data-stu-id="acf1d-106">DESCRIPTION</span></span>


## <span data-ttu-id="acf1d-107">示例</span><span class="sxs-lookup"><span data-stu-id="acf1d-107">EXAMPLES</span></span>

### <span data-ttu-id="acf1d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="acf1d-108">Example 1</span></span>
```powershell
PS C:\> New-AzsAcquiredPlan -PlanAcquisitionId $([Guid]::NewGuid()) -PlanId "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan" -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

AcquisitionId       : 718c7f7c-4868-479a-98ce-5caaa8f158c1
AcquisitionTime     : 3/12/2020 11:16:08 PM
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/acquiredPlan
                      s/718c7f7c-4868-479a-98ce-5caaa8f158c1
PlanId              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/plans/testplan
ProvisioningState   : Succeeded
```

<span data-ttu-id="acf1d-109">建立訂閱者案。</span><span class="sxs-lookup"><span data-stu-id="acf1d-109">Create a subscription plan.</span></span>

## <span data-ttu-id="acf1d-110">參數</span><span class="sxs-lookup"><span data-stu-id="acf1d-110">PARAMETERS</span></span>

### <span data-ttu-id="acf1d-111">-AcquiredPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="acf1d-111">-AcquiredPlanDefinition</span></span>
<span data-ttu-id="acf1d-112">若要建立，請參閱 ACQUIREDPLANDEFINITION 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="acf1d-112">To construct, see NOTES section for ACQUIREDPLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="acf1d-113">-AcquisitionTime</span><span class="sxs-lookup"><span data-stu-id="acf1d-113">-AcquisitionTime</span></span>


```yaml
Type: System.DateTime
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="acf1d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acf1d-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="acf1d-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="acf1d-115">-ExternalReferenceId</span></span>


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

### <span data-ttu-id="acf1d-116">-識別碼</span><span class="sxs-lookup"><span data-stu-id="acf1d-116">-Id</span></span>


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

### <span data-ttu-id="acf1d-117">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="acf1d-117">-PlanAcquisitionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="acf1d-118">-PlanId</span><span class="sxs-lookup"><span data-stu-id="acf1d-118">-PlanId</span></span>


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

### <span data-ttu-id="acf1d-119">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="acf1d-119">-ProvisioningState</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ProvisioningState
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="acf1d-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="acf1d-120">-SubscriptionId</span></span>


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

### <span data-ttu-id="acf1d-121">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="acf1d-121">-TargetSubscriptionId</span></span>


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

### <span data-ttu-id="acf1d-122">-確認</span><span class="sxs-lookup"><span data-stu-id="acf1d-122">-Confirm</span></span>
<span data-ttu-id="acf1d-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="acf1d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acf1d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acf1d-124">-WhatIf</span></span>
<span data-ttu-id="acf1d-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="acf1d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acf1d-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="acf1d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acf1d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acf1d-127">CommonParameters</span></span>
<span data-ttu-id="acf1d-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="acf1d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acf1d-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="acf1d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acf1d-130">輸入</span><span class="sxs-lookup"><span data-stu-id="acf1d-130">INPUTS</span></span>

### <span data-ttu-id="acf1d-131">IPlanAcquisition （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="acf1d-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

## <span data-ttu-id="acf1d-132">輸出</span><span class="sxs-lookup"><span data-stu-id="acf1d-132">OUTPUTS</span></span>

### <span data-ttu-id="acf1d-133">IPlanAcquisition （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="acf1d-133">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

<span data-ttu-id="acf1d-134">別名</span><span class="sxs-lookup"><span data-stu-id="acf1d-134">ALIASES</span></span>

<span data-ttu-id="acf1d-135">New-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="acf1d-135">New-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="acf1d-136">筆記</span><span class="sxs-lookup"><span data-stu-id="acf1d-136">NOTES</span></span>

<span data-ttu-id="acf1d-137">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="acf1d-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="acf1d-138">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="acf1d-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="acf1d-139">ACQUIREDPLANDEFINITION <IPlanAcquisition> ：</span><span class="sxs-lookup"><span data-stu-id="acf1d-139">ACQUIREDPLANDEFINITION <IPlanAcquisition>:</span></span> 
  - <span data-ttu-id="acf1d-140">`[AcquisitionId <String>]`：購置識別碼。</span><span class="sxs-lookup"><span data-stu-id="acf1d-140">`[AcquisitionId <String>]`: Acquisition identifier.</span></span>
  - <span data-ttu-id="acf1d-141">`[AcquisitionTime <DateTime?>]`：購置時間。</span><span class="sxs-lookup"><span data-stu-id="acf1d-141">`[AcquisitionTime <DateTime?>]`: Acquisition time.</span></span>
  - <span data-ttu-id="acf1d-142">`[ExternalReferenceId <String>]`：外部參照識別碼。</span><span class="sxs-lookup"><span data-stu-id="acf1d-142">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="acf1d-143">`[Id <String>]`：租使用者訂閱內容中的識別碼。</span><span class="sxs-lookup"><span data-stu-id="acf1d-143">`[Id <String>]`: Identifier in the tenant subscription context.</span></span>
  - <span data-ttu-id="acf1d-144">`[PlanId <String>]`：在租使用者訂閱內容中規劃識別碼。</span><span class="sxs-lookup"><span data-stu-id="acf1d-144">`[PlanId <String>]`: Plan identifier in the tenant subscription context.</span></span>
  - <span data-ttu-id="acf1d-145">`[ProvisioningState <ProvisioningState?>]`： [提供] 的狀態。</span><span class="sxs-lookup"><span data-stu-id="acf1d-145">`[ProvisioningState <ProvisioningState?>]`: State of the provisioning.</span></span>

## <span data-ttu-id="acf1d-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="acf1d-146">RELATED LINKS</span></span>

