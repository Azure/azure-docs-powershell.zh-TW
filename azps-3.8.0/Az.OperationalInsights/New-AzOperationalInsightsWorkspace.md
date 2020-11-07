---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 22cc5c18e2c3cf21472426160d667c7890f04d4f
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93968741"
---
# <span data-ttu-id="0f86e-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="0f86e-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="0f86e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0f86e-102">SYNOPSIS</span></span>
<span data-ttu-id="0f86e-103">建立工作區。</span><span class="sxs-lookup"><span data-stu-id="0f86e-103">Creates a workspace.</span></span>

## <span data-ttu-id="0f86e-104">句法</span><span class="sxs-lookup"><span data-stu-id="0f86e-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-CustomerId] <Guid>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f86e-105">說明</span><span class="sxs-lookup"><span data-stu-id="0f86e-105">DESCRIPTION</span></span>
<span data-ttu-id="0f86e-106">**新的-AzOperationalInsightsWorkspace** Cmdlet 會在指定的資源群組和位置中建立一個工作區。</span><span class="sxs-lookup"><span data-stu-id="0f86e-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="0f86e-107">示例</span><span class="sxs-lookup"><span data-stu-id="0f86e-107">EXAMPLES</span></span>

### <span data-ttu-id="0f86e-108">範例1：依名稱建立工作區</span><span class="sxs-lookup"><span data-stu-id="0f86e-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="0f86e-109">這個命令會在名為 [ContosoResourceGroup] 的資源群組中，建立名為 MyWorkspace 的標準 SKU 工作區。</span><span class="sxs-lookup"><span data-stu-id="0f86e-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="0f86e-110">範例2：建立工作區並將其連結至現有的帳戶</span><span class="sxs-lookup"><span data-stu-id="0f86e-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="0f86e-111">第一個命令使用 Get-AzOperationalInsightsLinkTargets Cmdlet 來取得 Operational Insights 帳戶連結目標，然後將它們儲存在 $OILinkTargets 變數中。</span><span class="sxs-lookup"><span data-stu-id="0f86e-111">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="0f86e-112">第二個命令會使用管線運算子，將 $OILinkTargets 中的第一個帳戶連結目標傳遞給 **AzOperationalInsightsWorkspace** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0f86e-112">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0f86e-113">此命令會建立一個名為 MyWorkspace 的標準 SKU 工作區，該工作區已連結至 $OILinkTargets 中第一個 Operational Insights 帳戶。</span><span class="sxs-lookup"><span data-stu-id="0f86e-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="0f86e-114">參數</span><span class="sxs-lookup"><span data-stu-id="0f86e-114">PARAMETERS</span></span>

### <span data-ttu-id="0f86e-115">-CustomerId</span><span class="sxs-lookup"><span data-stu-id="0f86e-115">-CustomerId</span></span>
<span data-ttu-id="0f86e-116">指定此工作區將連結到哪個帳戶。</span><span class="sxs-lookup"><span data-stu-id="0f86e-116">Specifies the account to which this workspace will be linked.</span></span>
<span data-ttu-id="0f86e-117">您也可以使用 Get-AzOperationalInsightsLinkTargets Cmdlet 來列出潛在的帳戶。</span><span class="sxs-lookup"><span data-stu-id="0f86e-117">The Get-AzOperationalInsightsLinkTargets cmdlet can also be used to list the potential accounts.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f86e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f86e-118">-DefaultProfile</span></span>
<span data-ttu-id="0f86e-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0f86e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f86e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="0f86e-120">-Force</span></span>
<span data-ttu-id="0f86e-121">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="0f86e-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0f86e-122">-位置</span><span class="sxs-lookup"><span data-stu-id="0f86e-122">-Location</span></span>
<span data-ttu-id="0f86e-123">指定要建立工作區的位置，例如 [東美國] 或 [西部]。</span><span class="sxs-lookup"><span data-stu-id="0f86e-123">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f86e-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="0f86e-124">-Name</span></span>
<span data-ttu-id="0f86e-125">指定工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f86e-125">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f86e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f86e-126">-ResourceGroupName</span></span>
<span data-ttu-id="0f86e-127">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f86e-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0f86e-128">工作區是在此資源群組中建立。</span><span class="sxs-lookup"><span data-stu-id="0f86e-128">The workspace is created in this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f86e-129">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="0f86e-129">-RetentionInDays</span></span>
<span data-ttu-id="0f86e-130">工作區資料保留天數（天）。</span><span class="sxs-lookup"><span data-stu-id="0f86e-130">The workspace data retention in days.</span></span> <span data-ttu-id="0f86e-131">730 days 是所有其他 Sku 允許的上限</span><span class="sxs-lookup"><span data-stu-id="0f86e-131">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f86e-132">-Sku</span><span class="sxs-lookup"><span data-stu-id="0f86e-132">-Sku</span></span>
<span data-ttu-id="0f86e-133">指定工作區的服務層級。</span><span class="sxs-lookup"><span data-stu-id="0f86e-133">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="0f86e-134">如需有關使用哪個值的詳細資訊，請核取 https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers 。</span><span class="sxs-lookup"><span data-stu-id="0f86e-134">For more information regarding which value to use please check https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="0f86e-135">有效值為：</span><span class="sxs-lookup"><span data-stu-id="0f86e-135">Valid values are:</span></span>
- <span data-ttu-id="0f86e-136">空閒</span><span class="sxs-lookup"><span data-stu-id="0f86e-136">free</span></span>
- <span data-ttu-id="0f86e-137">pergb2018</span><span class="sxs-lookup"><span data-stu-id="0f86e-137">pergb2018</span></span>
- <span data-ttu-id="0f86e-138">pernode</span><span class="sxs-lookup"><span data-stu-id="0f86e-138">pernode</span></span>
- <span data-ttu-id="0f86e-139">佳</span><span class="sxs-lookup"><span data-stu-id="0f86e-139">premium</span></span>
- <span data-ttu-id="0f86e-140">獨立</span><span class="sxs-lookup"><span data-stu-id="0f86e-140">standalone</span></span>
- <span data-ttu-id="0f86e-141">標準</span><span class="sxs-lookup"><span data-stu-id="0f86e-141">standard</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, pergb2018, pernode, premium, standalone, standard

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f86e-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="0f86e-142">-Tag</span></span>
<span data-ttu-id="0f86e-143">工作區的資源標記。</span><span class="sxs-lookup"><span data-stu-id="0f86e-143">The resource tags for the workspace.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f86e-144">-確認</span><span class="sxs-lookup"><span data-stu-id="0f86e-144">-Confirm</span></span>
<span data-ttu-id="0f86e-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0f86e-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f86e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f86e-146">-WhatIf</span></span>
<span data-ttu-id="0f86e-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0f86e-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f86e-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0f86e-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f86e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f86e-149">CommonParameters</span></span>
<span data-ttu-id="0f86e-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0f86e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f86e-151">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0f86e-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f86e-152">輸入</span><span class="sxs-lookup"><span data-stu-id="0f86e-152">INPUTS</span></span>

### <span data-ttu-id="0f86e-153">System.object</span><span class="sxs-lookup"><span data-stu-id="0f86e-153">System.String</span></span>

### <span data-ttu-id="0f86e-154">"CoreLib" 1 [[System. Guid.empty]、[System.] = 4.0.0.0、Culture = 中性、PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0f86e-154">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0f86e-155">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0f86e-155">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0f86e-156">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0f86e-156">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="0f86e-157">輸出</span><span class="sxs-lookup"><span data-stu-id="0f86e-157">OUTPUTS</span></span>

### <span data-ttu-id="0f86e-158">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="0f86e-158">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="0f86e-159">筆記</span><span class="sxs-lookup"><span data-stu-id="0f86e-159">NOTES</span></span>

<span data-ttu-id="0f86e-160">已發行新的定價模型。</span><span class="sxs-lookup"><span data-stu-id="0f86e-160">A new pricing model has been released.</span></span> <span data-ttu-id="0f86e-161">如果您是 CSP，表示您必須針對 sku 使用 "獨立主機"。</span><span class="sxs-lookup"><span data-stu-id="0f86e-161">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="0f86e-162">在幕後，sku 將會變更為 pergb2018。</span><span class="sxs-lookup"><span data-stu-id="0f86e-162">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="0f86e-163">如需詳細資訊，請參閱下列內容： https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="0f86e-163">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="0f86e-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="0f86e-164">RELATED LINKS</span></span>

[<span data-ttu-id="0f86e-165">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0f86e-165">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)
