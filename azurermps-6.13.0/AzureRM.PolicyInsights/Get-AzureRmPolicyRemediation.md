---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyRemediation.md
ms.openlocfilehash: e69ad25800dbf6aada7111a1093b4c878f3c0f9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453644"
---
# <span data-ttu-id="51d35-101">Get-AzureRmPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="51d35-101">Get-AzureRmPolicyRemediation</span></span>

## <span data-ttu-id="51d35-102">摘要</span><span class="sxs-lookup"><span data-stu-id="51d35-102">SYNOPSIS</span></span>
<span data-ttu-id="51d35-103">取得原則 remediations。</span><span class="sxs-lookup"><span data-stu-id="51d35-103">Gets policy remediations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51d35-104">句法</span><span class="sxs-lookup"><span data-stu-id="51d35-104">SYNTAX</span></span>

### <span data-ttu-id="51d35-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="51d35-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmPolicyRemediation [-Top <Int32>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="51d35-106">ByName</span><span class="sxs-lookup"><span data-stu-id="51d35-106">ByName</span></span>
```
Get-AzureRmPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-Top <Int32>] [-IncludeDetail] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="51d35-107">GenericScope</span><span class="sxs-lookup"><span data-stu-id="51d35-107">GenericScope</span></span>
```
Get-AzureRmPolicyRemediation -Scope <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51d35-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="51d35-108">ManagementGroupScope</span></span>
```
Get-AzureRmPolicyRemediation -ManagementGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51d35-109">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="51d35-109">ResourceGroupScope</span></span>
```
Get-AzureRmPolicyRemediation -ResourceGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51d35-110">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="51d35-110">ByResourceId</span></span>
```
Get-AzureRmPolicyRemediation -ResourceId <String> [-Top <Int32>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51d35-111">說明</span><span class="sxs-lookup"><span data-stu-id="51d35-111">DESCRIPTION</span></span>
<span data-ttu-id="51d35-112">**AzureRmPolicyRemediation** Cmdlet 會取得作用域或特定修正中的所有原則 remediations。</span><span class="sxs-lookup"><span data-stu-id="51d35-112">The **Get-AzureRmPolicyRemediation** cmdlet gets all policy remediations in a scope or a particular remediation.</span></span>

## <span data-ttu-id="51d35-113">示例</span><span class="sxs-lookup"><span data-stu-id="51d35-113">EXAMPLES</span></span>

### <span data-ttu-id="51d35-114">範例1：取得目前訂閱中的所有原則 remediations</span><span class="sxs-lookup"><span data-stu-id="51d35-114">Example 1: Get all policy remediations in the current subscription</span></span>
```
PS C:\> Select-AzureRmSubscription -Subscription "My Subscription"
PS C:\> Get-AzureRmPolicyRemediation
```

<span data-ttu-id="51d35-115">這個命令會取得在名為「我的訂閱」的訂閱或其下所建立的所有 remediations。</span><span class="sxs-lookup"><span data-stu-id="51d35-115">This command gets all the remediations created at or underneath a subscription named 'My Subscription'.</span></span>

### <span data-ttu-id="51d35-116">範例2：取得特定原則修正及部署詳細資料</span><span class="sxs-lookup"><span data-stu-id="51d35-116">Example 2: Get a specific policy remediation and the deployment details</span></span>
```
PS C:\> Get-AzureRmPolicyRemediation -ResourceGroupName "myResourceGroup" -Name "remediation1" -IncludeDetail
```

<span data-ttu-id="51d35-117">這個命令會從資源群組 ' myResourceGroup ' 取得名為「remediation1」的修正。</span><span class="sxs-lookup"><span data-stu-id="51d35-117">This command gets the remediation named 'remediation1' from resource group 'myResourceGroup'.</span></span> <span data-ttu-id="51d35-118">將會包含修正資源的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="51d35-118">The details of the resources being remediated will be included.</span></span>

### <span data-ttu-id="51d35-119">範例3：使用選擇性篩選，在管理群組中取得10個原則 remediations</span><span class="sxs-lookup"><span data-stu-id="51d35-119">Example 3: Get 10 policy remediations in a management group with optional filters</span></span>
```
PS C:\> Get-AzureRmPolicyRemediation -ManagementGroupName "mg1" -Top 10 -Filter "PolicyAssignmentId eq '/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1'"
```

<span data-ttu-id="51d35-120">這個命令會從名為「mg1」的管理群組中取得最多10個原則 remediations。</span><span class="sxs-lookup"><span data-stu-id="51d35-120">This command gets a max of 10 policy remediations from a management group named 'mg1'.</span></span> <span data-ttu-id="51d35-121">只會檢索指定原則指派的原則 remediations。</span><span class="sxs-lookup"><span data-stu-id="51d35-121">Only policy remediations for the given policy assignment will be retrieved.</span></span>

## <span data-ttu-id="51d35-122">參數</span><span class="sxs-lookup"><span data-stu-id="51d35-122">PARAMETERS</span></span>

### <span data-ttu-id="51d35-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51d35-123">-DefaultProfile</span></span>
<span data-ttu-id="51d35-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="51d35-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51d35-125">-篩選</span><span class="sxs-lookup"><span data-stu-id="51d35-125">-Filter</span></span>
<span data-ttu-id="51d35-126">使用 OData 符號篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="51d35-126">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="51d35-127">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="51d35-127">-IncludeDetail</span></span>
<span data-ttu-id="51d35-128">包括修正程式所建立之部署的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="51d35-128">Include details of the deployments created by the remediation.</span></span>

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

### <span data-ttu-id="51d35-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="51d35-129">-ManagementGroupName</span></span>
<span data-ttu-id="51d35-130">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="51d35-130">Management group ID.</span></span>

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

### <span data-ttu-id="51d35-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="51d35-131">-Name</span></span>
<span data-ttu-id="51d35-132">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="51d35-132">Resource name.</span></span>

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

### <span data-ttu-id="51d35-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51d35-133">-ResourceGroupName</span></span>
<span data-ttu-id="51d35-134">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="51d35-134">Resource group name.</span></span>

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

### <span data-ttu-id="51d35-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51d35-135">-ResourceId</span></span>
<span data-ttu-id="51d35-136">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="51d35-136">Resource ID.</span></span>

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

### <span data-ttu-id="51d35-137">-範圍</span><span class="sxs-lookup"><span data-stu-id="51d35-137">-Scope</span></span>
<span data-ttu-id="51d35-138">資源範圍。</span><span class="sxs-lookup"><span data-stu-id="51d35-138">Scope of the resource.</span></span> <span data-ttu-id="51d35-139">例如，"/subscriptions/{subscriptionId}/resourceGroups/{rgName}"。</span><span class="sxs-lookup"><span data-stu-id="51d35-139">For example, '/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="51d35-140">-上方</span><span class="sxs-lookup"><span data-stu-id="51d35-140">-Top</span></span>
<span data-ttu-id="51d35-141">要傳回的最大記錄數。</span><span class="sxs-lookup"><span data-stu-id="51d35-141">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="51d35-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51d35-142">CommonParameters</span></span>
<span data-ttu-id="51d35-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="51d35-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51d35-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="51d35-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51d35-145">輸入</span><span class="sxs-lookup"><span data-stu-id="51d35-145">INPUTS</span></span>

### <span data-ttu-id="51d35-146">System.object</span><span class="sxs-lookup"><span data-stu-id="51d35-146">System.String</span></span>

## <span data-ttu-id="51d35-147">輸出</span><span class="sxs-lookup"><span data-stu-id="51d35-147">OUTPUTS</span></span>

### <span data-ttu-id="51d35-148">PSRemediation 中的 PolicyInsights。</span><span class="sxs-lookup"><span data-stu-id="51d35-148">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="51d35-149">筆記</span><span class="sxs-lookup"><span data-stu-id="51d35-149">NOTES</span></span>

## <span data-ttu-id="51d35-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="51d35-150">RELATED LINKS</span></span>
