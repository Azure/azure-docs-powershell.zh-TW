---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/powershell/module/az.advisor/set-azadvisorConfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
ms.openlocfilehash: 550b9d11cd2f5b0cadb13d76809faa2ac34dc426
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905670"
---
# <span data-ttu-id="e6634-101">Set-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6634-101">Set-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="e6634-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e6634-102">SYNOPSIS</span></span>
<span data-ttu-id="e6634-103">更新或建立 Azure 建議程式組配置。</span><span class="sxs-lookup"><span data-stu-id="e6634-103">Updates or creates the Azure Advisor Configuration.</span></span>

## <span data-ttu-id="e6634-104">語法</span><span class="sxs-lookup"><span data-stu-id="e6634-104">SYNTAX</span></span>

### <span data-ttu-id="e6634-105">InputObjectRgExcludeParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e6634-105">InputObjectRgExcludeParameterSet (Default)</span></span>
```
Set-AzAdvisorConfiguration [-Exclude] [[-ResourceGroupName] <String>]
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6634-106">InputObjectLowObcludeParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6634-106">InputObjectLowCpuExcludeParameterSet</span></span> 
```
Set-AzAdvisorConfiguration [-Exclude] [-LowCpuThreshold] <Int32>
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6634-107">描述</span><span class="sxs-lookup"><span data-stu-id="e6634-107">DESCRIPTION</span></span>
<span data-ttu-id="e6634-108">用來更新 Azure Advisor 的組配置。</span><span class="sxs-lookup"><span data-stu-id="e6634-108">Used to update the configuration of the Azure Advisor.</span></span> <span data-ttu-id="e6634-109">有兩種類型的組組：訂閱層級組和 ResourceGroup 層級組組。</span><span class="sxs-lookup"><span data-stu-id="e6634-109">Two types of Configuration are present: Subscription level configuration and ResourceGroup level configuration.</span></span> 

<span data-ttu-id="e6634-110">訂閱層級組式：此類型的訂閱只能有一個組式。</span><span class="sxs-lookup"><span data-stu-id="e6634-110">Subscription level configuration: There can be only one Configuration for this type for a subscription.</span></span> <span data-ttu-id="e6634-111">您可以使用此 Cmdlet 更新 LowCmThreshold 和 Exclude 屬性。</span><span class="sxs-lookup"><span data-stu-id="e6634-111">LowCpuThreshold and Exclude properties can be updated using this cmdlet.</span></span>
<span data-ttu-id="e6634-112">ResourceGroup 層級組配置：每個 ResourceGroup 只能有一個組組。</span><span class="sxs-lookup"><span data-stu-id="e6634-112">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup.</span></span> <span data-ttu-id="e6634-113">只能使用此 Cmdlet 更新 Exclude 屬性。</span><span class="sxs-lookup"><span data-stu-id="e6634-113">Only Exclude property can be updated using this cmdlet.</span></span>

## <span data-ttu-id="e6634-114">例子</span><span class="sxs-lookup"><span data-stu-id="e6634-114">EXAMPLES</span></span>

###  <span data-ttu-id="e6634-115">範例 1</span><span class="sxs-lookup"><span data-stu-id="e6634-115">Example 1</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 10
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 10

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="e6634-116">更新訂閱層級 (的) 版 。</a0></span><span class="sxs-lookup"><span data-stu-id="e6634-116">Updates the configuration(lowCpuThreshold) for subscription level Configuration.</span></span>

### <span data-ttu-id="e6634-117">範例 2</span><span class="sxs-lookup"><span data-stu-id="e6634-117">Example 2</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 15 -Exclude 
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : 15

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="e6634-118">更新低 (的組配置、) 訂閱層級的組配置，以及建議產生排除專案。</span><span class="sxs-lookup"><span data-stu-id="e6634-118">Updates the configuration(lowCpuThreshold, exclude) for subscription level Configuration and excludes from the recommendation generation.</span></span>

### <span data-ttu-id="e6634-119">範例 3</span><span class="sxs-lookup"><span data-stu-id="e6634-119">Example 3</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -ResourceGroupName resourceGroupName1 -Exclude

Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}-resourceGroupName1
Name       : {user_subscription}-resourceGroupName1
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : null

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="e6634-120">更新組 (排除) 建議產生中要排除的資源GroupName1。</span><span class="sxs-lookup"><span data-stu-id="e6634-120">Updates the configuration(exclude) for resourceGroupName1 to be excluded in the recommendation generation.</span></span>

### <span data-ttu-id="e6634-121">範例 4</span><span class="sxs-lookup"><span data-stu-id="e6634-121">Example 4</span></span>
```powershell
PS C:\> Get-AzAdvisorConfiguration | Set-AzAdvisorConfiguration -LowCpuThreshold 20
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 20

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="e6634-122">更新從管線傳遞之給定建議的組配置。</span><span class="sxs-lookup"><span data-stu-id="e6634-122">Updates the configuration for the given recommendation passed on from the pipeline.</span></span>

## <span data-ttu-id="e6634-123">參數</span><span class="sxs-lookup"><span data-stu-id="e6634-123">PARAMETERS</span></span>

### <span data-ttu-id="e6634-124">-確認</span><span class="sxs-lookup"><span data-stu-id="e6634-124">-Confirm</span></span>
<span data-ttu-id="e6634-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e6634-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6634-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6634-126">-DefaultProfile</span></span>
<span data-ttu-id="e6634-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e6634-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6634-128">-排除</span><span class="sxs-lookup"><span data-stu-id="e6634-128">-Exclude</span></span>
<span data-ttu-id="e6634-129">從建議產生中排除。</span><span class="sxs-lookup"><span data-stu-id="e6634-129">Exclude from the recommendation generation.</span></span> <span data-ttu-id="e6634-130">如果未指定 exclude 屬性，會設為 False。</span><span class="sxs-lookup"><span data-stu-id="e6634-130">If not specified exclude property will be set to false.</span></span>

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

### <span data-ttu-id="e6634-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6634-131">-InputObject</span></span>
<span data-ttu-id="e6634-132">powershell 物件類型 PsAzureAdvisorConfigurationData 由 Get-AzAdvisorConfiguration呼叫。</span><span class="sxs-lookup"><span data-stu-id="e6634-132">The powershell object type PsAzureAdvisorConfigurationData returned by Get-AzAdvisorConfiguration call.</span></span>

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

### <span data-ttu-id="e6634-133">-LowThreshold</span><span class="sxs-lookup"><span data-stu-id="e6634-133">-LowCpuThreshold</span></span>
<span data-ttu-id="e6634-134">低 Cpu 閾值的值。</span><span class="sxs-lookup"><span data-stu-id="e6634-134">Value for Low Cpu threshold.</span></span>

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

### <span data-ttu-id="e6634-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6634-135">-ResourceGroupName</span></span>
<span data-ttu-id="e6634-136">組配置的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e6634-136">Resource Group name for the configuration.</span></span>

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

### <span data-ttu-id="e6634-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6634-137">-WhatIf</span></span>
<span data-ttu-id="e6634-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e6634-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6634-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e6634-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6634-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6634-140">CommonParameters</span></span>
<span data-ttu-id="e6634-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e6634-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e6634-142">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e6634-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6634-143">輸入</span><span class="sxs-lookup"><span data-stu-id="e6634-143">INPUTS</span></span>

### <span data-ttu-id="e6634-144">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="e6634-144">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="e6634-145">輸出</span><span class="sxs-lookup"><span data-stu-id="e6634-145">OUTPUTS</span></span>

### <span data-ttu-id="e6634-146">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="e6634-146">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="e6634-147">筆記</span><span class="sxs-lookup"><span data-stu-id="e6634-147">NOTES</span></span>

## <span data-ttu-id="e6634-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6634-148">RELATED LINKS</span></span>
