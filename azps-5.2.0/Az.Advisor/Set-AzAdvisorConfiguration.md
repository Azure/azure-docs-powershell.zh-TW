---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/set-azadvisorConfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
ms.openlocfilehash: bfd1677fa46a749b73206b02bb6585c4a529637f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278950"
---
# <span data-ttu-id="5b946-101">Set-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b946-101">Set-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="5b946-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5b946-102">SYNOPSIS</span></span>
<span data-ttu-id="5b946-103">更新或建立 Azure Advisor 配置。</span><span class="sxs-lookup"><span data-stu-id="5b946-103">Updates or creates the Azure Advisor Configuration.</span></span>

## <span data-ttu-id="5b946-104">句法</span><span class="sxs-lookup"><span data-stu-id="5b946-104">SYNTAX</span></span>

### <span data-ttu-id="5b946-105">InputObjectRgExcludeParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5b946-105">InputObjectRgExcludeParameterSet (Default)</span></span>
```
Set-AzAdvisorConfiguration [-Exclude] [[-ResourceGroupName] <String>]
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b946-106">InputObjectLowCpuExcludeParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b946-106">InputObjectLowCpuExcludeParameterSet</span></span> 
```
Set-AzAdvisorConfiguration [-Exclude] [-LowCpuThreshold] <Int32>
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b946-107">說明</span><span class="sxs-lookup"><span data-stu-id="5b946-107">DESCRIPTION</span></span>
<span data-ttu-id="5b946-108">用來更新 Azure Advisor 的設定。</span><span class="sxs-lookup"><span data-stu-id="5b946-108">Used to update the configuration of the Azure Advisor.</span></span> <span data-ttu-id="5b946-109">有兩種類型的設定：訂閱等級設定和 ResourceGroup 層級設定。</span><span class="sxs-lookup"><span data-stu-id="5b946-109">Two types of Configuration are present: Subscription level configuration and ResourceGroup level configuration.</span></span> 

<span data-ttu-id="5b946-110">訂閱階層配置：此類型只能有一個針對訂閱的配置。</span><span class="sxs-lookup"><span data-stu-id="5b946-110">Subscription level configuration: There can be only one Configuration for this type for a subscription.</span></span> <span data-ttu-id="5b946-111">LowCpuThreshold 和 Exclude 屬性可以使用此 Cmdlet 來更新。</span><span class="sxs-lookup"><span data-stu-id="5b946-111">LowCpuThreshold and Exclude properties can be updated using this cmdlet.</span></span>
<span data-ttu-id="5b946-112">ResourceGroup 層次配置：每個 ResourceGroup 只能有一個設定。</span><span class="sxs-lookup"><span data-stu-id="5b946-112">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup.</span></span> <span data-ttu-id="5b946-113">只有 Exclude 屬性可以使用此 Cmdlet 進行更新。</span><span class="sxs-lookup"><span data-stu-id="5b946-113">Only Exclude property can be updated using this cmdlet.</span></span>

## <span data-ttu-id="5b946-114">示例</span><span class="sxs-lookup"><span data-stu-id="5b946-114">EXAMPLES</span></span>

###  <span data-ttu-id="5b946-115">範例1</span><span class="sxs-lookup"><span data-stu-id="5b946-115">Example 1</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 10
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 10

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="5b946-116">更新訂閱層級設定 (lowCpuThreshold) 的設定。</span><span class="sxs-lookup"><span data-stu-id="5b946-116">Updates the configuration(lowCpuThreshold) for subscription level Configuration.</span></span>

### <span data-ttu-id="5b946-117">範例2</span><span class="sxs-lookup"><span data-stu-id="5b946-117">Example 2</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 15 -Exclude 
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : 15

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="5b946-118">更新 (lowCpuThreshold 的設定，排除訂閱層級設定的) ，並從建議的產生中排除。</span><span class="sxs-lookup"><span data-stu-id="5b946-118">Updates the configuration(lowCpuThreshold, exclude) for subscription level Configuration and excludes from the recommendation generation.</span></span>

### <span data-ttu-id="5b946-119">範例3</span><span class="sxs-lookup"><span data-stu-id="5b946-119">Example 3</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -ResourceGroupName resourceGroupName1 -Exclude

Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}-resourceGroupName1
Name       : {user_subscription}-resourceGroupName1
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : null

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="5b946-120">更新 (排除) 的設定，以在建議產生中排除 resourceGroupName1。</span><span class="sxs-lookup"><span data-stu-id="5b946-120">Updates the configuration(exclude) for resourceGroupName1 to be excluded in the recommendation generation.</span></span>

### <span data-ttu-id="5b946-121">範例4</span><span class="sxs-lookup"><span data-stu-id="5b946-121">Example 4</span></span>
```powershell
PS C:\> Get-AzAdvisorConfiguration | Set-AzAdvisorConfiguration -LowCpuThreshold 20
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 20

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="5b946-122">更新從管線傳遞之給定建議的設定。</span><span class="sxs-lookup"><span data-stu-id="5b946-122">Updates the configuration for the given recommendation passed on from the pipeline.</span></span>

## <span data-ttu-id="5b946-123">參數</span><span class="sxs-lookup"><span data-stu-id="5b946-123">PARAMETERS</span></span>

### <span data-ttu-id="5b946-124">-確認</span><span class="sxs-lookup"><span data-stu-id="5b946-124">-Confirm</span></span>
<span data-ttu-id="5b946-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5b946-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b946-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b946-126">-DefaultProfile</span></span>
<span data-ttu-id="5b946-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b946-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b946-128">-排除</span><span class="sxs-lookup"><span data-stu-id="5b946-128">-Exclude</span></span>
<span data-ttu-id="5b946-129">從建議的產生中排除。</span><span class="sxs-lookup"><span data-stu-id="5b946-129">Exclude from the recommendation generation.</span></span> <span data-ttu-id="5b946-130">如果未指定，exclude 屬性將會設定為 false。</span><span class="sxs-lookup"><span data-stu-id="5b946-130">If not specified exclude property will be set to false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b946-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b946-131">-InputObject</span></span>
<span data-ttu-id="5b946-132">Get-AzAdvisorConfiguration call 傳回的 powershell 物件類型 PsAzureAdvisorConfigurationData。</span><span class="sxs-lookup"><span data-stu-id="5b946-132">The powershell object type PsAzureAdvisorConfigurationData returned by Get-AzAdvisorConfiguration call.</span></span>

```yaml
Type: PsAzureAdvisorConfigurationData
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b946-133">-LowCpuThreshold</span><span class="sxs-lookup"><span data-stu-id="5b946-133">-LowCpuThreshold</span></span>
<span data-ttu-id="5b946-134">低 Cpu 閾值的值。</span><span class="sxs-lookup"><span data-stu-id="5b946-134">Value for Low Cpu threshold.</span></span>

```yaml
Type: Int32
Parameter Sets: InputObjectLowCpuExcludeParameterSet
Aliases:
Accepted values: 0, 5, 10, 15, 20

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b946-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b946-135">-ResourceGroupName</span></span>
<span data-ttu-id="5b946-136">配置的資源群組名稱。</span><span class="sxs-lookup"><span data-stu-id="5b946-136">Resource Group name for the configuration.</span></span>

```yaml
Type: String
Parameter Sets: InputObjectRgExcludeParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b946-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b946-137">-WhatIf</span></span>
<span data-ttu-id="5b946-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5b946-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b946-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5b946-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b946-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b946-140">CommonParameters</span></span>
<span data-ttu-id="5b946-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5b946-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5b946-142">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5b946-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b946-143">輸入</span><span class="sxs-lookup"><span data-stu-id="5b946-143">INPUTS</span></span>

### <span data-ttu-id="5b946-144">PsAzureAdvisorConfigurationData 中的 [...]</span><span class="sxs-lookup"><span data-stu-id="5b946-144">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="5b946-145">輸出</span><span class="sxs-lookup"><span data-stu-id="5b946-145">OUTPUTS</span></span>

### <span data-ttu-id="5b946-146">PsAzureAdvisorConfigurationData 中的 [...]</span><span class="sxs-lookup"><span data-stu-id="5b946-146">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="5b946-147">筆記</span><span class="sxs-lookup"><span data-stu-id="5b946-147">NOTES</span></span>

## <span data-ttu-id="5b946-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b946-148">RELATED LINKS</span></span>
