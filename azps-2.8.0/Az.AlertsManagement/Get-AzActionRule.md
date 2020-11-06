---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
ms.openlocfilehash: f3904826ef41f271086d048183b8b2035d1b11e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614136"
---
# <span data-ttu-id="3c1df-101">Get-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="3c1df-101">Get-AzActionRule</span></span>

## <span data-ttu-id="3c1df-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3c1df-102">SYNOPSIS</span></span>
<span data-ttu-id="3c1df-103">取得動作規則資訊</span><span class="sxs-lookup"><span data-stu-id="3c1df-103">Get Action Rules Information</span></span>

## <span data-ttu-id="3c1df-104">句法</span><span class="sxs-lookup"><span data-stu-id="3c1df-104">SYNTAX</span></span>

### <span data-ttu-id="3c1df-105">ListActionRules (預設) </span><span class="sxs-lookup"><span data-stu-id="3c1df-105">ListActionRules (Default)</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceType <String>]
 [-TargetResourceGroup <String>] [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>]
 [-AlertRuleId <String>] [-Description <String>] [-ActionGroup <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c1df-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c1df-106">ResourceId</span></span>
```
Get-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c1df-107">ActionRuleByName</span><span class="sxs-lookup"><span data-stu-id="3c1df-107">ActionRuleByName</span></span>
```
Get-AzActionRule -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3c1df-108">ListActionRulesByTargetResourceId</span><span class="sxs-lookup"><span data-stu-id="3c1df-108">ListActionRulesByTargetResourceId</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceId <String>]
 [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>] [-AlertRuleId <String>]
 [-Description <String>] [-ActionGroup <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c1df-109">說明</span><span class="sxs-lookup"><span data-stu-id="3c1df-109">DESCRIPTION</span></span>
<span data-ttu-id="3c1df-110">**AzActionRule** Cmdlet 會取得設定的動作規則。</span><span class="sxs-lookup"><span data-stu-id="3c1df-110">**Get-AzActionRule** cmdlet gets action rules configured.</span></span>

## <span data-ttu-id="3c1df-111">示例</span><span class="sxs-lookup"><span data-stu-id="3c1df-111">EXAMPLES</span></span>

### <span data-ttu-id="3c1df-112">範例1</span><span class="sxs-lookup"><span data-stu-id="3c1df-112">Example 1</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Severity "Sev2" -MonitorService "Platform"
```

<span data-ttu-id="3c1df-113">列出在 [資源群組測試] 中設定的所有動作規則，並篩選出 [Sev2 嚴重性] 和 [平臺監視器] 服務。</span><span class="sxs-lookup"><span data-stu-id="3c1df-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span></span> <span data-ttu-id="3c1df-114">使用 Format-List 來取得清單中每個動作規則的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3c1df-114">Use Format-List to get the details of each action rule in list.</span></span>

### <span data-ttu-id="3c1df-115">範例2</span><span class="sxs-lookup"><span data-stu-id="3c1df-115">Example 2</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Name "Test-Action-Rule" | Format-List
```

<span data-ttu-id="3c1df-116">在測試 rg 資源群組中取得名稱測試-動作規則的動作規則。</span><span class="sxs-lookup"><span data-stu-id="3c1df-116">Get the action rule with name Test-Action-Rule in test-rg resource group.</span></span>

## <span data-ttu-id="3c1df-117">參數</span><span class="sxs-lookup"><span data-stu-id="3c1df-117">PARAMETERS</span></span>

### <span data-ttu-id="3c1df-118">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="3c1df-118">-ActionGroup</span></span>
<span data-ttu-id="3c1df-119">[動作] 群組</span><span class="sxs-lookup"><span data-stu-id="3c1df-119">Action group</span></span>

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

### <span data-ttu-id="3c1df-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="3c1df-120">-AlertRuleId</span></span>
<span data-ttu-id="3c1df-121">篩選警示規則識別碼</span><span class="sxs-lookup"><span data-stu-id="3c1df-121">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="3c1df-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c1df-122">-DefaultProfile</span></span>
<span data-ttu-id="3c1df-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3c1df-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c1df-124">-描述</span><span class="sxs-lookup"><span data-stu-id="3c1df-124">-Description</span></span>
<span data-ttu-id="3c1df-125">篩選具有智慧群組識別碼的所有警示</span><span class="sxs-lookup"><span data-stu-id="3c1df-125">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="3c1df-126">-ImpactedScope</span><span class="sxs-lookup"><span data-stu-id="3c1df-126">-ImpactedScope</span></span>
<span data-ttu-id="3c1df-127">篩選受影響的範圍</span><span class="sxs-lookup"><span data-stu-id="3c1df-127">Filter on Impacted scope</span></span>

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

### <span data-ttu-id="3c1df-128">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="3c1df-128">-MonitorService</span></span>
<span data-ttu-id="3c1df-129">篩選 Moniter 服務</span><span class="sxs-lookup"><span data-stu-id="3c1df-129">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="3c1df-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="3c1df-130">-Name</span></span>
<span data-ttu-id="3c1df-131">行動規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c1df-131">Name of action rule.</span></span>

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

### <span data-ttu-id="3c1df-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c1df-132">-ResourceGroupName</span></span>
<span data-ttu-id="3c1df-133">動作規則所駐留的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c1df-133">Resource Group Name in which action rule resides.</span></span>

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

### <span data-ttu-id="3c1df-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c1df-134">-ResourceId</span></span>
<span data-ttu-id="3c1df-135">透過 resoure 識別碼取得動作規則。</span><span class="sxs-lookup"><span data-stu-id="3c1df-135">Get Action rule by resoure id.</span></span>

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

### <span data-ttu-id="3c1df-136">-嚴重度</span><span class="sxs-lookup"><span data-stu-id="3c1df-136">-Severity</span></span>
<span data-ttu-id="3c1df-137">在警示嚴重度篩選</span><span class="sxs-lookup"><span data-stu-id="3c1df-137">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="3c1df-138">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3c1df-138">-TargetResourceGroup</span></span>
<span data-ttu-id="3c1df-139">篩選 [警示] 目標資源的 [資源] 群組名稱。</span><span class="sxs-lookup"><span data-stu-id="3c1df-139">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="3c1df-140">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="3c1df-140">-TargetResourceId</span></span>
<span data-ttu-id="3c1df-141">篩選警報目標資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3c1df-141">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="3c1df-142">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="3c1df-142">-TargetResourceType</span></span>
<span data-ttu-id="3c1df-143">篩選警報目標資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="3c1df-143">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="3c1df-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c1df-144">CommonParameters</span></span>
<span data-ttu-id="3c1df-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3c1df-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c1df-146">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3c1df-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c1df-147">輸入</span><span class="sxs-lookup"><span data-stu-id="3c1df-147">INPUTS</span></span>

### <span data-ttu-id="3c1df-148">所有</span><span class="sxs-lookup"><span data-stu-id="3c1df-148">None</span></span>

## <span data-ttu-id="3c1df-149">輸出</span><span class="sxs-lookup"><span data-stu-id="3c1df-149">OUTPUTS</span></span>

### <span data-ttu-id="3c1df-150">AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="3c1df-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="3c1df-151">筆記</span><span class="sxs-lookup"><span data-stu-id="3c1df-151">NOTES</span></span>

## <span data-ttu-id="3c1df-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="3c1df-152">RELATED LINKS</span></span>
