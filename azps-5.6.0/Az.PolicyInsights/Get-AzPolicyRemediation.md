---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
ms.openlocfilehash: 352cfe453d6e965c23fd075615568eb1d22f1dd9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911370"
---
# <span data-ttu-id="342b4-101">Get-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="342b4-101">Get-AzPolicyRemediation</span></span>

## <span data-ttu-id="342b4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="342b4-102">SYNOPSIS</span></span>
<span data-ttu-id="342b4-103">獲得政策補救。</span><span class="sxs-lookup"><span data-stu-id="342b4-103">Gets policy remediations.</span></span>

## <span data-ttu-id="342b4-104">語法</span><span class="sxs-lookup"><span data-stu-id="342b4-104">SYNTAX</span></span>

### <span data-ttu-id="342b4-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="342b4-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyRemediation [-Top <Int32>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="342b4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="342b4-106">ByName</span></span>
```
Get-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-Top <Int32>] [-IncludeDetail] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="342b4-107">GenericScope</span><span class="sxs-lookup"><span data-stu-id="342b4-107">GenericScope</span></span>
```
Get-AzPolicyRemediation -Scope <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="342b4-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="342b4-108">ManagementGroupScope</span></span>
```
Get-AzPolicyRemediation -ManagementGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="342b4-109">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="342b4-109">ResourceGroupScope</span></span>
```
Get-AzPolicyRemediation -ResourceGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="342b4-110">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="342b4-110">ByResourceId</span></span>
```
Get-AzPolicyRemediation -ResourceId <String> [-Top <Int32>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="342b4-111">描述</span><span class="sxs-lookup"><span data-stu-id="342b4-111">DESCRIPTION</span></span>
<span data-ttu-id="342b4-112">**Get-AzPolicyRemediation** Cmdlet 會取得範圍或特定補救範圍內的所有策略補救。</span><span class="sxs-lookup"><span data-stu-id="342b4-112">The **Get-AzPolicyRemediation** cmdlet gets all policy remediations in a scope or a particular remediation.</span></span>

## <span data-ttu-id="342b4-113">例子</span><span class="sxs-lookup"><span data-stu-id="342b4-113">EXAMPLES</span></span>

### <span data-ttu-id="342b4-114">範例 1：取得目前訂閱中所有政策補救</span><span class="sxs-lookup"><span data-stu-id="342b4-114">Example 1: Get all policy remediations in the current subscription</span></span>
```
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Get-AzPolicyRemediation
```

<span data-ttu-id="342b4-115">此命令會獲得在名為"我的訂閱"的訂閱或下方建立的所有修復。</span><span class="sxs-lookup"><span data-stu-id="342b4-115">This command gets all the remediations created at or underneath a subscription named 'My Subscription'.</span></span>

### <span data-ttu-id="342b4-116">範例 2：取得特定的策略補救和部署詳細資料</span><span class="sxs-lookup"><span data-stu-id="342b4-116">Example 2: Get a specific policy remediation and the deployment details</span></span>
```
PS C:\> Get-AzPolicyRemediation -ResourceGroupName "myResourceGroup" -Name "remediation1" -IncludeDetail
```

<span data-ttu-id="342b4-117">此命令會從資源群組 "myResourceGroup" 獲得名為 "remediation1" 的補救。</span><span class="sxs-lookup"><span data-stu-id="342b4-117">This command gets the remediation named 'remediation1' from resource group 'myResourceGroup'.</span></span> <span data-ttu-id="342b4-118">將會包含要補救的資源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="342b4-118">The details of the resources being remediated will be included.</span></span>

### <span data-ttu-id="342b4-119">範例 3：在具有選擇性篩選的管理群組中取得 10 個策略補救</span><span class="sxs-lookup"><span data-stu-id="342b4-119">Example 3: Get 10 policy remediations in a management group with optional filters</span></span>
```
PS C:\> Get-AzPolicyRemediation -ManagementGroupName "mg1" -Top 10 -Filter "PolicyAssignmentId eq '/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1'"
```

<span data-ttu-id="342b4-120">此命令最多會從名為 'mg1' 的管理群組獲得 10 個策略補救。</span><span class="sxs-lookup"><span data-stu-id="342b4-120">This command gets a max of 10 policy remediations from a management group named 'mg1'.</span></span> <span data-ttu-id="342b4-121">系統只會針對指定之策略工作分派進行政策補救。</span><span class="sxs-lookup"><span data-stu-id="342b4-121">Only policy remediations for the given policy assignment will be retrieved.</span></span>

## <span data-ttu-id="342b4-122">參數</span><span class="sxs-lookup"><span data-stu-id="342b4-122">PARAMETERS</span></span>

### <span data-ttu-id="342b4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="342b4-123">-DefaultProfile</span></span>
<span data-ttu-id="342b4-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="342b4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="342b4-125">-篩選</span><span class="sxs-lookup"><span data-stu-id="342b4-125">-Filter</span></span>
<span data-ttu-id="342b4-126">使用 OData 標記法篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="342b4-126">Filter expression using OData notation.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, GenericScope, ManagementGroupScope, ResourceGroupScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="342b4-127">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="342b4-127">-IncludeDetail</span></span>
<span data-ttu-id="342b4-128">包含補救所建立之部署的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="342b4-128">Include details of the deployments created by the remediation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="342b4-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="342b4-129">-ManagementGroupName</span></span>
<span data-ttu-id="342b4-130">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="342b4-130">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="342b4-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="342b4-131">-Name</span></span>
<span data-ttu-id="342b4-132">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="342b4-132">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="342b4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="342b4-133">-ResourceGroupName</span></span>
<span data-ttu-id="342b4-134">資源組名。</span><span class="sxs-lookup"><span data-stu-id="342b4-134">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="342b4-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="342b4-135">-ResourceId</span></span>
<span data-ttu-id="342b4-136">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="342b4-136">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="342b4-137">-範圍</span><span class="sxs-lookup"><span data-stu-id="342b4-137">-Scope</span></span>
<span data-ttu-id="342b4-138">資源的範圍。</span><span class="sxs-lookup"><span data-stu-id="342b4-138">Scope of the resource.</span></span> <span data-ttu-id="342b4-139">例如，'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'。</span><span class="sxs-lookup"><span data-stu-id="342b4-139">For example, '/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GenericScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="342b4-140">-頂端</span><span class="sxs-lookup"><span data-stu-id="342b4-140">-Top</span></span>
<span data-ttu-id="342b4-141">要退回的記錄數目上限。</span><span class="sxs-lookup"><span data-stu-id="342b4-141">Maximum number of records to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="342b4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="342b4-142">CommonParameters</span></span>
<span data-ttu-id="342b4-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="342b4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="342b4-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="342b4-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="342b4-145">輸入</span><span class="sxs-lookup"><span data-stu-id="342b4-145">INPUTS</span></span>

### <span data-ttu-id="342b4-146">System.String</span><span class="sxs-lookup"><span data-stu-id="342b4-146">System.String</span></span>

## <span data-ttu-id="342b4-147">輸出</span><span class="sxs-lookup"><span data-stu-id="342b4-147">OUTPUTS</span></span>

### <span data-ttu-id="342b4-148">Microsoft.Azure.Commands.PolicyInsights.models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="342b4-148">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="342b4-149">筆記</span><span class="sxs-lookup"><span data-stu-id="342b4-149">NOTES</span></span>

## <span data-ttu-id="342b4-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="342b4-150">RELATED LINKS</span></span>
