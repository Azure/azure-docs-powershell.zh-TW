---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/set-azadvisorConfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
ms.openlocfilehash: 4c3a3fd8f80bf1f8a18f65a8dc5c9d0bf26b6d9b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614150"
---
# <span data-ttu-id="f3236-101">Set-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3236-101">Set-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="f3236-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3236-102">SYNOPSIS</span></span>
<span data-ttu-id="f3236-103">更新或建立 Azure Advisor 配置。</span><span class="sxs-lookup"><span data-stu-id="f3236-103">Updates or creates the Azure Advisor Configuration.</span></span>

## <span data-ttu-id="f3236-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3236-104">SYNTAX</span></span>

### <span data-ttu-id="f3236-105">InputObjectRgExcludeParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f3236-105">InputObjectRgExcludeParameterSet (Default)</span></span>
```
Set-AzAdvisorConfiguration [-Exclude] [[-ResourceGroupName] <String>]
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3236-106">InputObjectLowCpuExcludeParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3236-106">InputObjectLowCpuExcludeParameterSet</span></span> 
```
Set-AzAdvisorConfiguration [-Exclude] [-LowCpuThreshold] <Int32>
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3236-107">說明</span><span class="sxs-lookup"><span data-stu-id="f3236-107">DESCRIPTION</span></span>
<span data-ttu-id="f3236-108">用來更新 Azure Advisor 的設定。</span><span class="sxs-lookup"><span data-stu-id="f3236-108">Used to update the configuration of the Azure Advisor.</span></span> <span data-ttu-id="f3236-109">有兩種類型的設定：訂閱等級設定和 ResourceGroup 層級設定。</span><span class="sxs-lookup"><span data-stu-id="f3236-109">Two types of Configuration are present: Subscription level configuration and ResourceGroup level configuration.</span></span> 

<span data-ttu-id="f3236-110">訂閱階層配置：此類型只能有一個針對訂閱的配置。</span><span class="sxs-lookup"><span data-stu-id="f3236-110">Subscription level configuration: There can be only one Configuration for this type for a subscription.</span></span> <span data-ttu-id="f3236-111">LowCpuThreshold 和 Exclude 屬性可以使用此 Cmdlet 來更新。</span><span class="sxs-lookup"><span data-stu-id="f3236-111">LowCpuThreshold and Exclude properties can be updated using this cmdlet.</span></span>
<span data-ttu-id="f3236-112">ResourceGroup 層次配置：每個 ResourceGroup 只能有一個設定。</span><span class="sxs-lookup"><span data-stu-id="f3236-112">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup.</span></span> <span data-ttu-id="f3236-113">只有 Exclude 屬性可以使用此 Cmdlet 進行更新。</span><span class="sxs-lookup"><span data-stu-id="f3236-113">Only Exclude property can be updated using this cmdlet.</span></span>

## <span data-ttu-id="f3236-114">示例</span><span class="sxs-lookup"><span data-stu-id="f3236-114">EXAMPLES</span></span>

###  <span data-ttu-id="f3236-115">範例1</span><span class="sxs-lookup"><span data-stu-id="f3236-115">Example 1</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 10
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 10

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="f3236-116">更新訂閱層級設定 (lowCpuThreshold) 的設定。</span><span class="sxs-lookup"><span data-stu-id="f3236-116">Updates the configuration(lowCpuThreshold) for subscription level Configuration.</span></span>

### <span data-ttu-id="f3236-117">範例2</span><span class="sxs-lookup"><span data-stu-id="f3236-117">Example 2</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 15 -Exclude 
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : 15

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="f3236-118">更新 (lowCpuThreshold 的設定，排除訂閱層級設定的) ，並從建議的產生中排除。</span><span class="sxs-lookup"><span data-stu-id="f3236-118">Updates the configuration(lowCpuThreshold, exclude) for subscription level Configuration and excludes from the recommendation generation.</span></span>

### <span data-ttu-id="f3236-119">範例3</span><span class="sxs-lookup"><span data-stu-id="f3236-119">Example 3</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -ResourceGroupName resourceGroupName1 -Exclude

Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}-resourceGroupName1
Name       : {user_subscription}-resourceGroupName1
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : null

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="f3236-120">更新 (排除) 的設定，以在建議產生中排除 resourceGroupName1。</span><span class="sxs-lookup"><span data-stu-id="f3236-120">Updates the configuration(exclude) for resourceGroupName1 to be excluded in the recommendation generation.</span></span>

### <span data-ttu-id="f3236-121">範例4</span><span class="sxs-lookup"><span data-stu-id="f3236-121">Example 4</span></span>
```powershell
PS C:\> Get-AzAdvisorConfiguration | Set-AzAdvisorConfiguration -LowCpuThreshold 20
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 20

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="f3236-122">更新從管線傳遞之給定建議的設定。</span><span class="sxs-lookup"><span data-stu-id="f3236-122">Updates the configuration for the given recommendation passed on from the pipeline.</span></span>

## <span data-ttu-id="f3236-123">參數</span><span class="sxs-lookup"><span data-stu-id="f3236-123">PARAMETERS</span></span>

### <span data-ttu-id="f3236-124">-確認</span><span class="sxs-lookup"><span data-stu-id="f3236-124">-Confirm</span></span>
<span data-ttu-id="f3236-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f3236-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3236-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3236-126">-DefaultProfile</span></span>
<span data-ttu-id="f3236-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3236-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3236-128">-排除</span><span class="sxs-lookup"><span data-stu-id="f3236-128">-Exclude</span></span>
<span data-ttu-id="f3236-129">從建議的產生中排除。</span><span class="sxs-lookup"><span data-stu-id="f3236-129">Exclude from the recommendation generation.</span></span> <span data-ttu-id="f3236-130">如果未指定，exclude 屬性將會設定為 false。</span><span class="sxs-lookup"><span data-stu-id="f3236-130">If not specified exclude property will be set to false.</span></span>

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

### <span data-ttu-id="f3236-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3236-131">-InputObject</span></span>
<span data-ttu-id="f3236-132">Get-AzAdvisorConfiguration call 傳回的 powershell 物件類型 PsAzureAdvisorConfigurationData。</span><span class="sxs-lookup"><span data-stu-id="f3236-132">The powershell object type PsAzureAdvisorConfigurationData returned by Get-AzAdvisorConfiguration call.</span></span>

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

### <span data-ttu-id="f3236-133">-LowCpuThreshold</span><span class="sxs-lookup"><span data-stu-id="f3236-133">-LowCpuThreshold</span></span>
<span data-ttu-id="f3236-134">低 Cpu 閾值的值。</span><span class="sxs-lookup"><span data-stu-id="f3236-134">Value for Low Cpu threshold.</span></span>

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

### <span data-ttu-id="f3236-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3236-135">-ResourceGroupName</span></span>
<span data-ttu-id="f3236-136">配置的資源群組名稱。</span><span class="sxs-lookup"><span data-stu-id="f3236-136">Resource Group name for the configuration.</span></span>

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

### <span data-ttu-id="f3236-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3236-137">-WhatIf</span></span>
<span data-ttu-id="f3236-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f3236-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3236-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f3236-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3236-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3236-140">CommonParameters</span></span>
<span data-ttu-id="f3236-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3236-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f3236-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f3236-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3236-143">輸入</span><span class="sxs-lookup"><span data-stu-id="f3236-143">INPUTS</span></span>

### <span data-ttu-id="f3236-144">PsAzureAdvisorConfigurationData 中的 [...]</span><span class="sxs-lookup"><span data-stu-id="f3236-144">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="f3236-145">輸出</span><span class="sxs-lookup"><span data-stu-id="f3236-145">OUTPUTS</span></span>

### <span data-ttu-id="f3236-146">PsAzureAdvisorConfigurationData 中的 [...]</span><span class="sxs-lookup"><span data-stu-id="f3236-146">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="f3236-147">筆記</span><span class="sxs-lookup"><span data-stu-id="f3236-147">NOTES</span></span>

## <span data-ttu-id="f3236-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3236-148">RELATED LINKS</span></span>