---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 8515bf4085fcd03d87aa15c3da649fe318b94966
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405001"
---
# <span data-ttu-id="54980-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="54980-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="54980-102">簡介</span><span class="sxs-lookup"><span data-stu-id="54980-102">SYNOPSIS</span></span>
<span data-ttu-id="54980-103">建立工作區。</span><span class="sxs-lookup"><span data-stu-id="54980-103">Creates a workspace.</span></span>

## <span data-ttu-id="54980-104">語法</span><span class="sxs-lookup"><span data-stu-id="54980-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [[-PublicNetworkAccessForIngestion] <String>]
 [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54980-105">描述</span><span class="sxs-lookup"><span data-stu-id="54980-105">DESCRIPTION</span></span>
<span data-ttu-id="54980-106">**New-AzOperationalInsightsWorkspace** Cmdlet 會建立指定資源群組和位置中的工作區。</span><span class="sxs-lookup"><span data-stu-id="54980-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="54980-107">例子</span><span class="sxs-lookup"><span data-stu-id="54980-107">EXAMPLES</span></span>

### <span data-ttu-id="54980-108">範例 1：根據名稱建立工作區</span><span class="sxs-lookup"><span data-stu-id="54980-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="54980-109">此命令在名為 ContosoResourceGroup 的資源群組中，建立名為 MyWorkspace 的標準 SKU 工作區。</span><span class="sxs-lookup"><span data-stu-id="54980-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="54980-110">範例 2：建立工作區，並連結至現有帳戶</span><span class="sxs-lookup"><span data-stu-id="54980-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="54980-111">第一個命令使用 Get-AzOperationalInsightsLinkTargets Cmdlet 取得營運深入資訊帳戶連結目標，然後將它們儲存在 $OILinkTargets 變數中。</span><span class="sxs-lookup"><span data-stu-id="54980-111">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="54980-112">第二個命令會使用管線運算子，將 $OILinkTargets 中的第一個帳戶連結目標傳遞至 **New-AzOperationalInsightsWorkspace** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54980-112">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="54980-113">該命令會建立名為 MyWorkspace 的標準 SKU 工作區，該工作區會連結至 $OILinkTargets 中第一個營運深入資訊帳戶。</span><span class="sxs-lookup"><span data-stu-id="54980-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="54980-114">參數</span><span class="sxs-lookup"><span data-stu-id="54980-114">PARAMETERS</span></span>

### <span data-ttu-id="54980-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54980-115">-DefaultProfile</span></span>
<span data-ttu-id="54980-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="54980-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54980-117">-強制</span><span class="sxs-lookup"><span data-stu-id="54980-117">-Force</span></span>
<span data-ttu-id="54980-118">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="54980-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="54980-119">-位置</span><span class="sxs-lookup"><span data-stu-id="54980-119">-Location</span></span>
<span data-ttu-id="54980-120">指定建立工作區的位置，例如美國東部或西歐。</span><span class="sxs-lookup"><span data-stu-id="54980-120">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="54980-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="54980-121">-Name</span></span>
<span data-ttu-id="54980-122">指定工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="54980-122">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="54980-123">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="54980-123">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="54980-124">存取工作區輸入的網路存取類型。</span><span class="sxs-lookup"><span data-stu-id="54980-124">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="54980-125">值應為 'Enabled' 或 'Disabled'</span><span class="sxs-lookup"><span data-stu-id="54980-125">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="54980-126">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="54980-126">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="54980-127">存取工作區查詢的網路存取類型。</span><span class="sxs-lookup"><span data-stu-id="54980-127">The network access type for accessing workspace query.</span></span> <span data-ttu-id="54980-128">值應為 'Enabled' 或 'Disabled'</span><span class="sxs-lookup"><span data-stu-id="54980-128">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="54980-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54980-129">-ResourceGroupName</span></span>
<span data-ttu-id="54980-130">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="54980-130">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="54980-131">此資源群組中已建立工作區。</span><span class="sxs-lookup"><span data-stu-id="54980-131">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="54980-132">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="54980-132">-RetentionInDays</span></span>
<span data-ttu-id="54980-133">工作區資料保留天數。</span><span class="sxs-lookup"><span data-stu-id="54980-133">The workspace data retention in days.</span></span> <span data-ttu-id="54980-134">所有其他 SKU 的允許上限為 730 天</span><span class="sxs-lookup"><span data-stu-id="54980-134">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="54980-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="54980-135">-Sku</span></span>
<span data-ttu-id="54980-136">指定工作區的服務層級。</span><span class="sxs-lookup"><span data-stu-id="54980-136">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="54980-137">如需有關要使用哪個值的資訊，請檢查 https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers 。</span><span class="sxs-lookup"><span data-stu-id="54980-137">For more information regarding which value to use please check https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="54980-138">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="54980-138">Valid values are:</span></span>
- <span data-ttu-id="54980-139">自由</span><span class="sxs-lookup"><span data-stu-id="54980-139">free</span></span>
- <span data-ttu-id="54980-140">pergb2018</span><span class="sxs-lookup"><span data-stu-id="54980-140">pergb2018</span></span>
- <span data-ttu-id="54980-141">pernode</span><span class="sxs-lookup"><span data-stu-id="54980-141">pernode</span></span>
- <span data-ttu-id="54980-142">溢價</span><span class="sxs-lookup"><span data-stu-id="54980-142">premium</span></span>
- <span data-ttu-id="54980-143">獨立</span><span class="sxs-lookup"><span data-stu-id="54980-143">standalone</span></span>
- <span data-ttu-id="54980-144">標準</span><span class="sxs-lookup"><span data-stu-id="54980-144">standard</span></span>

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

### <span data-ttu-id="54980-145">-標記</span><span class="sxs-lookup"><span data-stu-id="54980-145">-Tag</span></span>
<span data-ttu-id="54980-146">工作區的資源標記。</span><span class="sxs-lookup"><span data-stu-id="54980-146">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="54980-147">-確認</span><span class="sxs-lookup"><span data-stu-id="54980-147">-Confirm</span></span>
<span data-ttu-id="54980-148">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="54980-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54980-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54980-149">-WhatIf</span></span>
<span data-ttu-id="54980-150">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="54980-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54980-151">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54980-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54980-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54980-152">CommonParameters</span></span>
<span data-ttu-id="54980-153">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="54980-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54980-154">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54980-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54980-155">輸入</span><span class="sxs-lookup"><span data-stu-id="54980-155">INPUTS</span></span>

### <span data-ttu-id="54980-156">System.String</span><span class="sxs-lookup"><span data-stu-id="54980-156">System.String</span></span>

### <span data-ttu-id="54980-157">System.Nullable'1[[System.Guid， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="54980-157">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="54980-158">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="54980-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="54980-159">System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="54980-159">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="54980-160">輸出</span><span class="sxs-lookup"><span data-stu-id="54980-160">OUTPUTS</span></span>

### <span data-ttu-id="54980-161">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="54980-161">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="54980-162">筆記</span><span class="sxs-lookup"><span data-stu-id="54980-162">NOTES</span></span>

<span data-ttu-id="54980-163">已發行新的定價模型。</span><span class="sxs-lookup"><span data-stu-id="54980-163">A new pricing model has been released.</span></span> <span data-ttu-id="54980-164">如果您是 CSP，這表示您必須針對 SKU 使用「獨立」。</span><span class="sxs-lookup"><span data-stu-id="54980-164">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="54980-165">在幕後，SKU 將會變更為 pergb2018。</span><span class="sxs-lookup"><span data-stu-id="54980-165">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="54980-166">如需詳細資訊，請參閱下列專案： https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="54980-166">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="54980-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="54980-167">RELATED LINKS</span></span>

[<span data-ttu-id="54980-168">Azure 營運深入資訊 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="54980-168">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)



