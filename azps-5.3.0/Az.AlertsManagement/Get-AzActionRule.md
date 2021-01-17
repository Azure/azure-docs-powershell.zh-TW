---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
ms.openlocfilehash: 59ce466233e4997f54ed8f29835e7e64d455fb86
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437723"
---
# <span data-ttu-id="f8d7c-101">Get-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="f8d7c-101">Get-AzActionRule</span></span>

## <span data-ttu-id="f8d7c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f8d7c-102">SYNOPSIS</span></span>
<span data-ttu-id="f8d7c-103">取得動作規則資訊</span><span class="sxs-lookup"><span data-stu-id="f8d7c-103">Get Action Rules Information</span></span>

## <span data-ttu-id="f8d7c-104">句法</span><span class="sxs-lookup"><span data-stu-id="f8d7c-104">SYNTAX</span></span>

### <span data-ttu-id="f8d7c-105">ListActionRules (預設) </span><span class="sxs-lookup"><span data-stu-id="f8d7c-105">ListActionRules (Default)</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceType <String>]
 [-TargetResourceGroup <String>] [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>]
 [-AlertRuleId <String>] [-Description <String>] [-ActionGroup <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8d7c-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8d7c-106">ResourceId</span></span>
```
Get-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8d7c-107">ActionRuleByName</span><span class="sxs-lookup"><span data-stu-id="f8d7c-107">ActionRuleByName</span></span>
```
Get-AzActionRule -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8d7c-108">ListActionRulesByTargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f8d7c-108">ListActionRulesByTargetResourceId</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceId <String>]
 [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>] [-AlertRuleId <String>]
 [-Description <String>] [-ActionGroup <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8d7c-109">說明</span><span class="sxs-lookup"><span data-stu-id="f8d7c-109">DESCRIPTION</span></span>
<span data-ttu-id="f8d7c-110">**AzActionRule** Cmdlet 會取得設定的動作規則。</span><span class="sxs-lookup"><span data-stu-id="f8d7c-110">**Get-AzActionRule** cmdlet gets action rules configured.</span></span>

## <span data-ttu-id="f8d7c-111">示例</span><span class="sxs-lookup"><span data-stu-id="f8d7c-111">EXAMPLES</span></span>

### <span data-ttu-id="f8d7c-112">範例1</span><span class="sxs-lookup"><span data-stu-id="f8d7c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Severity "Sev2" -MonitorService "Platform"
```

<span data-ttu-id="f8d7c-113">列出在 [資源群組測試] 中設定的所有動作規則，並篩選出 [Sev2 嚴重性] 和 [平臺監視器] 服務。</span><span class="sxs-lookup"><span data-stu-id="f8d7c-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span></span> <span data-ttu-id="f8d7c-114">使用 Format-List 來取得清單中每個動作規則的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f8d7c-114">Use Format-List to get the details of each action rule in list.</span></span>

### <span data-ttu-id="f8d7c-115">範例2</span><span class="sxs-lookup"><span data-stu-id="f8d7c-115">Example 2</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Name "Test-Action-Rule" | Format-List
```

<span data-ttu-id="f8d7c-116">在測試 rg 資源群組中取得名稱測試-動作規則的動作規則。</span><span class="sxs-lookup"><span data-stu-id="f8d7c-116">Get the action rule with name Test-Action-Rule in test-rg resource group.</span></span>

## <span data-ttu-id="f8d7c-117">參數</span><span class="sxs-lookup"><span data-stu-id="f8d7c-117">PARAMETERS</span></span>

### <span data-ttu-id="f8d7c-118">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="f8d7c-118">-ActionGroup</span></span>
<span data-ttu-id="f8d7c-119">[動作] 群組</span><span class="sxs-lookup"><span data-stu-id="f8d7c-119">Action group</span></span>

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

### <span data-ttu-id="f8d7c-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="f8d7c-120">-AlertRuleId</span></span>
<span data-ttu-id="f8d7c-121">篩選警示規則識別碼</span><span class="sxs-lookup"><span data-stu-id="f8d7c-121">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="f8d7c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8d7c-122">-DefaultProfile</span></span>
<span data-ttu-id="f8d7c-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f8d7c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8d7c-124">-描述</span><span class="sxs-lookup"><span data-stu-id="f8d7c-124">-Description</span></span>
<span data-ttu-id="f8d7c-125">篩選具有智慧群組識別碼的所有警示</span><span class="sxs-lookup"><span data-stu-id="f8d7c-125">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="f8d7c-126">-ImpactedScope</span><span class="sxs-lookup"><span data-stu-id="f8d7c-126">-ImpactedScope</span></span>
<span data-ttu-id="f8d7c-127">篩選受影響的範圍</span><span class="sxs-lookup"><span data-stu-id="f8d7c-127">Filter on Impacted scope</span></span>

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

### <span data-ttu-id="f8d7c-128">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="f8d7c-128">-MonitorService</span></span>
<span data-ttu-id="f8d7c-129">篩選 Moniter 服務</span><span class="sxs-lookup"><span data-stu-id="f8d7c-129">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="f8d7c-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="f8d7c-130">-Name</span></span>
<span data-ttu-id="f8d7c-131">行動規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8d7c-131">Name of action rule.</span></span>

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

### <span data-ttu-id="f8d7c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8d7c-132">-ResourceGroupName</span></span>
<span data-ttu-id="f8d7c-133">動作規則所駐留的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8d7c-133">Resource Group Name in which action rule resides.</span></span>

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

### <span data-ttu-id="f8d7c-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8d7c-134">-ResourceId</span></span>
<span data-ttu-id="f8d7c-135">依資源識別碼取得動作規則。</span><span class="sxs-lookup"><span data-stu-id="f8d7c-135">Get Action rule by resource id.</span></span>

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

### <span data-ttu-id="f8d7c-136">-嚴重度</span><span class="sxs-lookup"><span data-stu-id="f8d7c-136">-Severity</span></span>
<span data-ttu-id="f8d7c-137">在警示嚴重度篩選</span><span class="sxs-lookup"><span data-stu-id="f8d7c-137">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="f8d7c-138">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f8d7c-138">-TargetResourceGroup</span></span>
<span data-ttu-id="f8d7c-139">篩選 [警示] 目標資源的 [資源] 群組名稱。</span><span class="sxs-lookup"><span data-stu-id="f8d7c-139">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="f8d7c-140">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f8d7c-140">-TargetResourceId</span></span>
<span data-ttu-id="f8d7c-141">篩選警報目標資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f8d7c-141">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="f8d7c-142">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="f8d7c-142">-TargetResourceType</span></span>
<span data-ttu-id="f8d7c-143">篩選警報目標資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="f8d7c-143">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="f8d7c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8d7c-144">CommonParameters</span></span>
<span data-ttu-id="f8d7c-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f8d7c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8d7c-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f8d7c-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8d7c-147">輸入</span><span class="sxs-lookup"><span data-stu-id="f8d7c-147">INPUTS</span></span>

### <span data-ttu-id="f8d7c-148">所有</span><span class="sxs-lookup"><span data-stu-id="f8d7c-148">None</span></span>

## <span data-ttu-id="f8d7c-149">輸出</span><span class="sxs-lookup"><span data-stu-id="f8d7c-149">OUTPUTS</span></span>

### <span data-ttu-id="f8d7c-150">AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="f8d7c-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="f8d7c-151">筆記</span><span class="sxs-lookup"><span data-stu-id="f8d7c-151">NOTES</span></span>

## <span data-ttu-id="f8d7c-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8d7c-152">RELATED LINKS</span></span>
