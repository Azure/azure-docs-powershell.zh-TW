---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/new-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentOrganization.md
ms.openlocfilehash: 546b4e56f2a932a6d7f17bda8484db8cd1c3c593
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917065"
---
# <span data-ttu-id="cd91b-101">New-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="cd91b-101">New-AzConfluentOrganization</span></span>

## <span data-ttu-id="cd91b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cd91b-102">SYNOPSIS</span></span>
<span data-ttu-id="cd91b-103">建立組織資源</span><span class="sxs-lookup"><span data-stu-id="cd91b-103">Create Organization resource</span></span>

## <span data-ttu-id="cd91b-104">語法</span><span class="sxs-lookup"><span data-stu-id="cd91b-104">SYNTAX</span></span>

```
New-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Location <String>] [-OfferDetailId <String>] [-OfferDetailPlanId <String>] [-OfferDetailPlanName <String>]
 [-OfferDetailPublisherId <String>] [-OfferDetailStatus <SaaSOfferStatus>] [-OfferDetailTermUnit <String>]
 [-Tag <Hashtable>] [-UserDetailEmailAddress <String>] [-UserDetailFirstName <String>]
 [-UserDetailLastName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="cd91b-105">描述</span><span class="sxs-lookup"><span data-stu-id="cd91b-105">DESCRIPTION</span></span>
<span data-ttu-id="cd91b-106">建立組織資源</span><span class="sxs-lookup"><span data-stu-id="cd91b-106">Create Organization resource</span></span>

## <span data-ttu-id="cd91b-107">例子</span><span class="sxs-lookup"><span data-stu-id="cd91b-107">EXAMPLES</span></span>

### <span data-ttu-id="cd91b-108">範例 1：建立一個多餘的組織</span><span class="sxs-lookup"><span data-stu-id="cd91b-108">Example 1: Create a confluent organization</span></span>
```powershell
PS C:\> New-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh -Location eastus -OfferDetailId "confluent-cloud-azure-prod" -OfferDetailPlanId "confluent-cloud-azure-payg-prod" -OfferDetailPlanName "Confluent Cloud - Pay as you Go" -OfferDetailPublisherId "confluentinc" -OfferDetailTermUnit "P1M" -UserDetailEmailAddress "xxxx@microsoft.com"

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="cd91b-109">此命令會建立一個不必要的組織。</span><span class="sxs-lookup"><span data-stu-id="cd91b-109">This command creates a confluent organization.</span></span>

## <span data-ttu-id="cd91b-110">參數</span><span class="sxs-lookup"><span data-stu-id="cd91b-110">PARAMETERS</span></span>

### <span data-ttu-id="cd91b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd91b-111">-AsJob</span></span>
<span data-ttu-id="cd91b-112">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="cd91b-112">Run the command as a job</span></span>

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

### <span data-ttu-id="cd91b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd91b-113">-DefaultProfile</span></span>
<span data-ttu-id="cd91b-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cd91b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd91b-115">-位置</span><span class="sxs-lookup"><span data-stu-id="cd91b-115">-Location</span></span>
<span data-ttu-id="cd91b-116">組織資源的位置</span><span class="sxs-lookup"><span data-stu-id="cd91b-116">Location of Organization resource</span></span>

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

### <span data-ttu-id="cd91b-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="cd91b-117">-Name</span></span>
<span data-ttu-id="cd91b-118">組織資源名稱</span><span class="sxs-lookup"><span data-stu-id="cd91b-118">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd91b-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cd91b-119">-NoWait</span></span>
<span data-ttu-id="cd91b-120">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="cd91b-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cd91b-121">-OfferDetailId</span><span class="sxs-lookup"><span data-stu-id="cd91b-121">-OfferDetailId</span></span>
<span data-ttu-id="cd91b-122">優惠識別碼</span><span class="sxs-lookup"><span data-stu-id="cd91b-122">Offer Id</span></span>

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

### <span data-ttu-id="cd91b-123">-OfferDetailPlanId</span><span class="sxs-lookup"><span data-stu-id="cd91b-123">-OfferDetailPlanId</span></span>
<span data-ttu-id="cd91b-124">優惠方案識別碼</span><span class="sxs-lookup"><span data-stu-id="cd91b-124">Offer Plan Id</span></span>

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

### <span data-ttu-id="cd91b-125">-OfferDetailPlanName</span><span class="sxs-lookup"><span data-stu-id="cd91b-125">-OfferDetailPlanName</span></span>
<span data-ttu-id="cd91b-126">優惠方案名稱</span><span class="sxs-lookup"><span data-stu-id="cd91b-126">Offer Plan Name</span></span>

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

### <span data-ttu-id="cd91b-127">-OfferDetailPublisherId</span><span class="sxs-lookup"><span data-stu-id="cd91b-127">-OfferDetailPublisherId</span></span>
<span data-ttu-id="cd91b-128">Publisher Id</span><span class="sxs-lookup"><span data-stu-id="cd91b-128">Publisher Id</span></span>

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

### <span data-ttu-id="cd91b-129">-OfferDetailStatus</span><span class="sxs-lookup"><span data-stu-id="cd91b-129">-OfferDetailStatus</span></span>
<span data-ttu-id="cd91b-130">SaaS 優惠狀態</span><span class="sxs-lookup"><span data-stu-id="cd91b-130">SaaS Offer Status</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Support.SaaSOfferStatus
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd91b-131">-OfferDetailTermUnit</span><span class="sxs-lookup"><span data-stu-id="cd91b-131">-OfferDetailTermUnit</span></span>
<span data-ttu-id="cd91b-132">優惠方案期限單位</span><span class="sxs-lookup"><span data-stu-id="cd91b-132">Offer Plan Term unit</span></span>

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

### <span data-ttu-id="cd91b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd91b-133">-ResourceGroupName</span></span>
<span data-ttu-id="cd91b-134">資源組名</span><span class="sxs-lookup"><span data-stu-id="cd91b-134">Resource group name</span></span>

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

### <span data-ttu-id="cd91b-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd91b-135">-SubscriptionId</span></span>
<span data-ttu-id="cd91b-136">Microsoft Azure 訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="cd91b-136">Microsoft Azure subscription id</span></span>

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

### <span data-ttu-id="cd91b-137">-標記</span><span class="sxs-lookup"><span data-stu-id="cd91b-137">-Tag</span></span>
<span data-ttu-id="cd91b-138">組織資源標記</span><span class="sxs-lookup"><span data-stu-id="cd91b-138">Organization resource tags</span></span>

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

### <span data-ttu-id="cd91b-139">-UserDetailEmailAddress</span><span class="sxs-lookup"><span data-stu-id="cd91b-139">-UserDetailEmailAddress</span></span>
<span data-ttu-id="cd91b-140">電子郵件地址</span><span class="sxs-lookup"><span data-stu-id="cd91b-140">Email address</span></span>

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

### <span data-ttu-id="cd91b-141">-UserDetailFirstName</span><span class="sxs-lookup"><span data-stu-id="cd91b-141">-UserDetailFirstName</span></span>
<span data-ttu-id="cd91b-142">名字</span><span class="sxs-lookup"><span data-stu-id="cd91b-142">First name</span></span>

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

### <span data-ttu-id="cd91b-143">-UserDetailLastName</span><span class="sxs-lookup"><span data-stu-id="cd91b-143">-UserDetailLastName</span></span>
<span data-ttu-id="cd91b-144">姓氏</span><span class="sxs-lookup"><span data-stu-id="cd91b-144">Last name</span></span>

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

### <span data-ttu-id="cd91b-145">-確認</span><span class="sxs-lookup"><span data-stu-id="cd91b-145">-Confirm</span></span>
<span data-ttu-id="cd91b-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cd91b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd91b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd91b-147">-WhatIf</span></span>
<span data-ttu-id="cd91b-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cd91b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd91b-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd91b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd91b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd91b-150">CommonParameters</span></span>
<span data-ttu-id="cd91b-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cd91b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd91b-152">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd91b-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd91b-153">輸入</span><span class="sxs-lookup"><span data-stu-id="cd91b-153">INPUTS</span></span>

## <span data-ttu-id="cd91b-154">輸出</span><span class="sxs-lookup"><span data-stu-id="cd91b-154">OUTPUTS</span></span>

### <span data-ttu-id="cd91b-155">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span><span class="sxs-lookup"><span data-stu-id="cd91b-155">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span></span>

## <span data-ttu-id="cd91b-156">筆記</span><span class="sxs-lookup"><span data-stu-id="cd91b-156">NOTES</span></span>

<span data-ttu-id="cd91b-157">別名</span><span class="sxs-lookup"><span data-stu-id="cd91b-157">ALIASES</span></span>

## <span data-ttu-id="cd91b-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd91b-158">RELATED LINKS</span></span>

