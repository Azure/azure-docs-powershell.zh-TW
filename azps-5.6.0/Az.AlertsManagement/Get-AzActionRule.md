---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/get-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
ms.openlocfilehash: c90c4ba559bfe6e453a984546217692181f40597
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904182"
---
# <span data-ttu-id="554dc-101">Get-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="554dc-101">Get-AzActionRule</span></span>

## <span data-ttu-id="554dc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="554dc-102">SYNOPSIS</span></span>
<span data-ttu-id="554dc-103">取得動作規則資訊</span><span class="sxs-lookup"><span data-stu-id="554dc-103">Get Action Rules Information</span></span>

## <span data-ttu-id="554dc-104">語法</span><span class="sxs-lookup"><span data-stu-id="554dc-104">SYNTAX</span></span>

### <span data-ttu-id="554dc-105">ListActionRules (預設) </span><span class="sxs-lookup"><span data-stu-id="554dc-105">ListActionRules (Default)</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceType <String>]
 [-TargetResourceGroup <String>] [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>]
 [-AlertRuleId <String>] [-Description <String>] [-ActionGroup <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="554dc-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="554dc-106">ResourceId</span></span>
```
Get-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="554dc-107">ActionRuleByName</span><span class="sxs-lookup"><span data-stu-id="554dc-107">ActionRuleByName</span></span>
```
Get-AzActionRule -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="554dc-108">ListActionRulesByTargetResourceId</span><span class="sxs-lookup"><span data-stu-id="554dc-108">ListActionRulesByTargetResourceId</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceId <String>]
 [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>] [-AlertRuleId <String>]
 [-Description <String>] [-ActionGroup <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="554dc-109">描述</span><span class="sxs-lookup"><span data-stu-id="554dc-109">DESCRIPTION</span></span>
<span data-ttu-id="554dc-110">**Get-AzActionRule** Cmdlet 會進行動作規則。</span><span class="sxs-lookup"><span data-stu-id="554dc-110">**Get-AzActionRule** cmdlet gets action rules configured.</span></span>

## <span data-ttu-id="554dc-111">例子</span><span class="sxs-lookup"><span data-stu-id="554dc-111">EXAMPLES</span></span>

### <span data-ttu-id="554dc-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="554dc-112">Example 1</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Severity "Sev2" -MonitorService "Platform"
```

<span data-ttu-id="554dc-113">列出在資源群組 test-rg 中根據 Sev2 嚴重性和平臺監視器服務篩選的所有動作規則。</span><span class="sxs-lookup"><span data-stu-id="554dc-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span></span> <span data-ttu-id="554dc-114">使用Format-List取得清單中每個動作規則的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="554dc-114">Use Format-List to get the details of each action rule in list.</span></span>

### <span data-ttu-id="554dc-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="554dc-115">Example 2</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Name "Test-Action-Rule" | Format-List
```

<span data-ttu-id="554dc-116">取得 test-rg 資源群組中名稱 Test-Action-Rule 的動作規則。</span><span class="sxs-lookup"><span data-stu-id="554dc-116">Get the action rule with name Test-Action-Rule in test-rg resource group.</span></span>

## <span data-ttu-id="554dc-117">參數</span><span class="sxs-lookup"><span data-stu-id="554dc-117">PARAMETERS</span></span>

### <span data-ttu-id="554dc-118">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="554dc-118">-ActionGroup</span></span>
<span data-ttu-id="554dc-119">動作群組</span><span class="sxs-lookup"><span data-stu-id="554dc-119">Action group</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="554dc-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="554dc-120">-AlertRuleId</span></span>
<span data-ttu-id="554dc-121">篩選警示規則識別碼</span><span class="sxs-lookup"><span data-stu-id="554dc-121">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="554dc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="554dc-122">-DefaultProfile</span></span>
<span data-ttu-id="554dc-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="554dc-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="554dc-124">-描述</span><span class="sxs-lookup"><span data-stu-id="554dc-124">-Description</span></span>
<span data-ttu-id="554dc-125">篩選所有具有智慧組識別碼的警示</span><span class="sxs-lookup"><span data-stu-id="554dc-125">Filter all the alerts having the Smart Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="554dc-126">-ImpactedScope</span><span class="sxs-lookup"><span data-stu-id="554dc-126">-ImpactedScope</span></span>
<span data-ttu-id="554dc-127">篩選影響的範圍</span><span class="sxs-lookup"><span data-stu-id="554dc-127">Filter on Impacted scope</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="554dc-128">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="554dc-128">-MonitorService</span></span>
<span data-ttu-id="554dc-129">在 Moniter Service 上篩選</span><span class="sxs-lookup"><span data-stu-id="554dc-129">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="554dc-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="554dc-130">-Name</span></span>
<span data-ttu-id="554dc-131">動作規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="554dc-131">Name of action rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ActionRuleByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="554dc-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="554dc-132">-ResourceGroupName</span></span>
<span data-ttu-id="554dc-133">動作規則所在的資源組名。</span><span class="sxs-lookup"><span data-stu-id="554dc-133">Resource Group Name in which action rule resides.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ActionRuleByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="554dc-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="554dc-134">-ResourceId</span></span>
<span data-ttu-id="554dc-135">依資源識別碼取得動作規則。</span><span class="sxs-lookup"><span data-stu-id="554dc-135">Get Action rule by resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="554dc-136">-嚴重性</span><span class="sxs-lookup"><span data-stu-id="554dc-136">-Severity</span></span>
<span data-ttu-id="554dc-137">篩選警示嚴重性</span><span class="sxs-lookup"><span data-stu-id="554dc-137">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="554dc-138">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="554dc-138">-TargetResourceGroup</span></span>
<span data-ttu-id="554dc-139">篩選警示目標資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="554dc-139">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="554dc-140">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="554dc-140">-TargetResourceId</span></span>
<span data-ttu-id="554dc-141">篩選警示目標資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="554dc-141">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="554dc-142">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="554dc-142">-TargetResourceType</span></span>
<span data-ttu-id="554dc-143">篩選警示目標資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="554dc-143">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="554dc-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="554dc-144">CommonParameters</span></span>
<span data-ttu-id="554dc-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="554dc-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="554dc-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="554dc-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="554dc-147">輸入</span><span class="sxs-lookup"><span data-stu-id="554dc-147">INPUTS</span></span>

### <span data-ttu-id="554dc-148">沒有</span><span class="sxs-lookup"><span data-stu-id="554dc-148">None</span></span>

## <span data-ttu-id="554dc-149">輸出</span><span class="sxs-lookup"><span data-stu-id="554dc-149">OUTPUTS</span></span>

### <span data-ttu-id="554dc-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="554dc-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="554dc-151">筆記</span><span class="sxs-lookup"><span data-stu-id="554dc-151">NOTES</span></span>

## <span data-ttu-id="554dc-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="554dc-152">RELATED LINKS</span></span>
