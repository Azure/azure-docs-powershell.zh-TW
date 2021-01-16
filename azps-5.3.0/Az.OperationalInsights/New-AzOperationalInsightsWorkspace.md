---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 50920451ca96d21875352ff2ef460a5dcc989a20
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437423"
---
# <span data-ttu-id="a609b-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="a609b-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="a609b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a609b-102">SYNOPSIS</span></span>
<span data-ttu-id="a609b-103">建立工作區，或還原虛刪除的工作區。</span><span class="sxs-lookup"><span data-stu-id="a609b-103">Creates a workspace, or restore a soft-deleted workspace.</span></span>

## <span data-ttu-id="a609b-104">句法</span><span class="sxs-lookup"><span data-stu-id="a609b-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [[-PublicNetworkAccessForIngestion] <String>]
 [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a609b-105">說明</span><span class="sxs-lookup"><span data-stu-id="a609b-105">DESCRIPTION</span></span>
<span data-ttu-id="a609b-106">**新的-AzOperationalInsightsWorkspace** Cmdlet 會在指定的資源群組和位置中建立一個工作區。</span><span class="sxs-lookup"><span data-stu-id="a609b-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span> <span data-ttu-id="a609b-107">或還原虛刪除的工作區。</span><span class="sxs-lookup"><span data-stu-id="a609b-107">Or restore a soft-deleted workspace.</span></span>

## <span data-ttu-id="a609b-108">示例</span><span class="sxs-lookup"><span data-stu-id="a609b-108">EXAMPLES</span></span>

### <span data-ttu-id="a609b-109">範例1：依名稱建立工作區</span><span class="sxs-lookup"><span data-stu-id="a609b-109">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="a609b-110">這個命令會在名為 [ContosoResourceGroup] 的資源群組中，建立名為 MyWorkspace 的標準 SKU 工作區。</span><span class="sxs-lookup"><span data-stu-id="a609b-110">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="a609b-111">範例2：建立工作區並將其連結至現有的帳戶</span><span class="sxs-lookup"><span data-stu-id="a609b-111">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="a609b-112">第一個命令使用 Get-AzOperationalInsightsLinkTargets Cmdlet 來取得 Operational Insights 帳戶連結目標，然後將它們儲存在 $OILinkTargets 變數中。</span><span class="sxs-lookup"><span data-stu-id="a609b-112">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="a609b-113">第二個命令會使用管線運算子，將 $OILinkTargets 中的第一個帳戶連結目標傳遞給 **AzOperationalInsightsWorkspace** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a609b-113">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a609b-114">此命令會建立一個名為 MyWorkspace 的標準 SKU 工作區，該工作區已連結至 $OILinkTargets 中第一個 Operational Insights 帳戶。</span><span class="sxs-lookup"><span data-stu-id="a609b-114">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="a609b-115">參數</span><span class="sxs-lookup"><span data-stu-id="a609b-115">PARAMETERS</span></span>

### <span data-ttu-id="a609b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a609b-116">-DefaultProfile</span></span>
<span data-ttu-id="a609b-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a609b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a609b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a609b-118">-Force</span></span>
<span data-ttu-id="a609b-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="a609b-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a609b-120">-位置</span><span class="sxs-lookup"><span data-stu-id="a609b-120">-Location</span></span>
<span data-ttu-id="a609b-121">指定要建立工作區的位置，例如 [東美國] 或 [西部]。</span><span class="sxs-lookup"><span data-stu-id="a609b-121">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="a609b-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="a609b-122">-Name</span></span>
<span data-ttu-id="a609b-123">指定工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="a609b-123">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="a609b-124">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="a609b-124">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="a609b-125">存取工作區接收的網路存取類型。</span><span class="sxs-lookup"><span data-stu-id="a609b-125">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="a609b-126">值應為 [Enabled] 或 "Disabled"</span><span class="sxs-lookup"><span data-stu-id="a609b-126">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a609b-127">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="a609b-127">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="a609b-128">用於存取工作區查詢的網路存取類型。</span><span class="sxs-lookup"><span data-stu-id="a609b-128">The network access type for accessing workspace query.</span></span> <span data-ttu-id="a609b-129">值應為 [Enabled] 或 "Disabled"</span><span class="sxs-lookup"><span data-stu-id="a609b-129">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a609b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a609b-130">-ResourceGroupName</span></span>
<span data-ttu-id="a609b-131">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a609b-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a609b-132">工作區是在此資源群組中建立。</span><span class="sxs-lookup"><span data-stu-id="a609b-132">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="a609b-133">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="a609b-133">-RetentionInDays</span></span>
<span data-ttu-id="a609b-134">工作區資料保留天數（天）。</span><span class="sxs-lookup"><span data-stu-id="a609b-134">The workspace data retention in days.</span></span> <span data-ttu-id="a609b-135">730 days 是所有其他 Sku 允許的上限</span><span class="sxs-lookup"><span data-stu-id="a609b-135">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="a609b-136">-Sku</span><span class="sxs-lookup"><span data-stu-id="a609b-136">-Sku</span></span>
<span data-ttu-id="a609b-137">指定工作區的服務層級。</span><span class="sxs-lookup"><span data-stu-id="a609b-137">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="a609b-138">如需有關使用哪個值的詳細資訊，請核取 https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers 。</span><span class="sxs-lookup"><span data-stu-id="a609b-138">For more information regarding which value to use please check https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="a609b-139">有效值為：</span><span class="sxs-lookup"><span data-stu-id="a609b-139">Valid values are:</span></span>
- <span data-ttu-id="a609b-140">空閒</span><span class="sxs-lookup"><span data-stu-id="a609b-140">free</span></span>
- <span data-ttu-id="a609b-141">pergb2018</span><span class="sxs-lookup"><span data-stu-id="a609b-141">pergb2018</span></span>
- <span data-ttu-id="a609b-142">pernode</span><span class="sxs-lookup"><span data-stu-id="a609b-142">pernode</span></span>
- <span data-ttu-id="a609b-143">佳</span><span class="sxs-lookup"><span data-stu-id="a609b-143">premium</span></span>
- <span data-ttu-id="a609b-144">獨立</span><span class="sxs-lookup"><span data-stu-id="a609b-144">standalone</span></span>
- <span data-ttu-id="a609b-145">標準</span><span class="sxs-lookup"><span data-stu-id="a609b-145">standard</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a609b-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="a609b-146">-Tag</span></span>
<span data-ttu-id="a609b-147">工作區的資源標記。</span><span class="sxs-lookup"><span data-stu-id="a609b-147">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="a609b-148">-確認</span><span class="sxs-lookup"><span data-stu-id="a609b-148">-Confirm</span></span>
<span data-ttu-id="a609b-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a609b-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a609b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a609b-150">-WhatIf</span></span>
<span data-ttu-id="a609b-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a609b-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a609b-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a609b-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a609b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a609b-153">CommonParameters</span></span>
<span data-ttu-id="a609b-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a609b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a609b-155">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a609b-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a609b-156">輸入</span><span class="sxs-lookup"><span data-stu-id="a609b-156">INPUTS</span></span>

### <span data-ttu-id="a609b-157">System.object</span><span class="sxs-lookup"><span data-stu-id="a609b-157">System.String</span></span>

### <span data-ttu-id="a609b-158">"CoreLib" 1 [[System. Guid.empty]、[System.] = 4.0.0.0、Culture = 中性、PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a609b-158">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a609b-159">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a609b-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a609b-160">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a609b-160">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a609b-161">輸出</span><span class="sxs-lookup"><span data-stu-id="a609b-161">OUTPUTS</span></span>

### <span data-ttu-id="a609b-162">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="a609b-162">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="a609b-163">筆記</span><span class="sxs-lookup"><span data-stu-id="a609b-163">NOTES</span></span>

<span data-ttu-id="a609b-164">已發行新的定價模型。</span><span class="sxs-lookup"><span data-stu-id="a609b-164">A new pricing model has been released.</span></span> <span data-ttu-id="a609b-165">如果您是 CSP，表示您必須針對 sku 使用 "獨立主機"。</span><span class="sxs-lookup"><span data-stu-id="a609b-165">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="a609b-166">在幕後，sku 將會變更為 pergb2018。</span><span class="sxs-lookup"><span data-stu-id="a609b-166">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="a609b-167">如需詳細資訊，請參閱下列內容： https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="a609b-167">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="a609b-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="a609b-168">RELATED LINKS</span></span>

[<span data-ttu-id="a609b-169">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a609b-169">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="a609b-170">AzOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="a609b-170">Get-AzOperationalInsightsLinkTargets</span></span>](./Get-AzOperationalInsightsLinkTargets.md)


