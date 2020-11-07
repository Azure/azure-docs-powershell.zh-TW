---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
ms.openlocfilehash: 44c12e08ca66c19cf3541f4abb200e1ba0663208
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965917"
---
# <span data-ttu-id="7fc92-101">Get-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="7fc92-101">Get-AzPolicyRemediation</span></span>

## <span data-ttu-id="7fc92-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7fc92-102">SYNOPSIS</span></span>
<span data-ttu-id="7fc92-103">取得原則 remediations。</span><span class="sxs-lookup"><span data-stu-id="7fc92-103">Gets policy remediations.</span></span>

## <span data-ttu-id="7fc92-104">句法</span><span class="sxs-lookup"><span data-stu-id="7fc92-104">SYNTAX</span></span>

### <span data-ttu-id="7fc92-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="7fc92-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyRemediation [-Top <Int32>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7fc92-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7fc92-106">ByName</span></span>
```
Get-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-Top <Int32>] [-IncludeDetail] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7fc92-107">GenericScope</span><span class="sxs-lookup"><span data-stu-id="7fc92-107">GenericScope</span></span>
```
Get-AzPolicyRemediation -Scope <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7fc92-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="7fc92-108">ManagementGroupScope</span></span>
```
Get-AzPolicyRemediation -ManagementGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7fc92-109">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="7fc92-109">ResourceGroupScope</span></span>
```
Get-AzPolicyRemediation -ResourceGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7fc92-110">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7fc92-110">ByResourceId</span></span>
```
Get-AzPolicyRemediation -ResourceId <String> [-Top <Int32>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fc92-111">說明</span><span class="sxs-lookup"><span data-stu-id="7fc92-111">DESCRIPTION</span></span>
<span data-ttu-id="7fc92-112">**AzPolicyRemediation** Cmdlet 會取得作用域或特定修正中的所有原則 remediations。</span><span class="sxs-lookup"><span data-stu-id="7fc92-112">The **Get-AzPolicyRemediation** cmdlet gets all policy remediations in a scope or a particular remediation.</span></span>

## <span data-ttu-id="7fc92-113">示例</span><span class="sxs-lookup"><span data-stu-id="7fc92-113">EXAMPLES</span></span>

### <span data-ttu-id="7fc92-114">範例1：取得目前訂閱中的所有原則 remediations</span><span class="sxs-lookup"><span data-stu-id="7fc92-114">Example 1: Get all policy remediations in the current subscription</span></span>
```
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Get-AzPolicyRemediation
```

<span data-ttu-id="7fc92-115">這個命令會取得在名為「我的訂閱」的訂閱或其下所建立的所有 remediations。</span><span class="sxs-lookup"><span data-stu-id="7fc92-115">This command gets all the remediations created at or underneath a subscription named 'My Subscription'.</span></span>

### <span data-ttu-id="7fc92-116">範例2：取得特定原則修正及部署詳細資料</span><span class="sxs-lookup"><span data-stu-id="7fc92-116">Example 2: Get a specific policy remediation and the deployment details</span></span>
```
PS C:\> Get-AzPolicyRemediation -ResourceGroupName "myResourceGroup" -Name "remediation1" -IncludeDetail
```

<span data-ttu-id="7fc92-117">這個命令會從資源群組 ' myResourceGroup ' 取得名為「remediation1」的修正。</span><span class="sxs-lookup"><span data-stu-id="7fc92-117">This command gets the remediation named 'remediation1' from resource group 'myResourceGroup'.</span></span> <span data-ttu-id="7fc92-118">將會包含修正資源的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7fc92-118">The details of the resources being remediated will be included.</span></span>

### <span data-ttu-id="7fc92-119">範例3：使用選擇性篩選，在管理群組中取得10個原則 remediations</span><span class="sxs-lookup"><span data-stu-id="7fc92-119">Example 3: Get 10 policy remediations in a management group with optional filters</span></span>
```
PS C:\> Get-AzPolicyRemediation -ManagementGroupName "mg1" -Top 10 -Filter "PolicyAssignmentId eq '/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1'"
```

<span data-ttu-id="7fc92-120">這個命令會從名為「mg1」的管理群組中取得最多10個原則 remediations。</span><span class="sxs-lookup"><span data-stu-id="7fc92-120">This command gets a max of 10 policy remediations from a management group named 'mg1'.</span></span> <span data-ttu-id="7fc92-121">只會檢索指定原則指派的原則 remediations。</span><span class="sxs-lookup"><span data-stu-id="7fc92-121">Only policy remediations for the given policy assignment will be retrieved.</span></span>

## <span data-ttu-id="7fc92-122">參數</span><span class="sxs-lookup"><span data-stu-id="7fc92-122">PARAMETERS</span></span>

### <span data-ttu-id="7fc92-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fc92-123">-DefaultProfile</span></span>
<span data-ttu-id="7fc92-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7fc92-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fc92-125">-篩選</span><span class="sxs-lookup"><span data-stu-id="7fc92-125">-Filter</span></span>
<span data-ttu-id="7fc92-126">使用 OData 符號篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="7fc92-126">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="7fc92-127">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="7fc92-127">-IncludeDetail</span></span>
<span data-ttu-id="7fc92-128">包括修正程式所建立之部署的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7fc92-128">Include details of the deployments created by the remediation.</span></span>

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

### <span data-ttu-id="7fc92-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="7fc92-129">-ManagementGroupName</span></span>
<span data-ttu-id="7fc92-130">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="7fc92-130">Management group ID.</span></span>

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

### <span data-ttu-id="7fc92-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="7fc92-131">-Name</span></span>
<span data-ttu-id="7fc92-132">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="7fc92-132">Resource name.</span></span>

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

### <span data-ttu-id="7fc92-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fc92-133">-ResourceGroupName</span></span>
<span data-ttu-id="7fc92-134">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="7fc92-134">Resource group name.</span></span>

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

### <span data-ttu-id="7fc92-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fc92-135">-ResourceId</span></span>
<span data-ttu-id="7fc92-136">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="7fc92-136">Resource ID.</span></span>

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

### <span data-ttu-id="7fc92-137">-範圍</span><span class="sxs-lookup"><span data-stu-id="7fc92-137">-Scope</span></span>
<span data-ttu-id="7fc92-138">資源範圍。</span><span class="sxs-lookup"><span data-stu-id="7fc92-138">Scope of the resource.</span></span> <span data-ttu-id="7fc92-139">例如，"/subscriptions/{subscriptionId}/resourceGroups/{rgName}"。</span><span class="sxs-lookup"><span data-stu-id="7fc92-139">For example, '/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="7fc92-140">-上方</span><span class="sxs-lookup"><span data-stu-id="7fc92-140">-Top</span></span>
<span data-ttu-id="7fc92-141">要傳回的最大記錄數。</span><span class="sxs-lookup"><span data-stu-id="7fc92-141">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="7fc92-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fc92-142">CommonParameters</span></span>
<span data-ttu-id="7fc92-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7fc92-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fc92-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7fc92-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fc92-145">輸入</span><span class="sxs-lookup"><span data-stu-id="7fc92-145">INPUTS</span></span>

### <span data-ttu-id="7fc92-146">System.object</span><span class="sxs-lookup"><span data-stu-id="7fc92-146">System.String</span></span>

## <span data-ttu-id="7fc92-147">輸出</span><span class="sxs-lookup"><span data-stu-id="7fc92-147">OUTPUTS</span></span>

### <span data-ttu-id="7fc92-148">PSRemediation 中的 PolicyInsights。</span><span class="sxs-lookup"><span data-stu-id="7fc92-148">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="7fc92-149">筆記</span><span class="sxs-lookup"><span data-stu-id="7fc92-149">NOTES</span></span>

## <span data-ttu-id="7fc92-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="7fc92-150">RELATED LINKS</span></span>
