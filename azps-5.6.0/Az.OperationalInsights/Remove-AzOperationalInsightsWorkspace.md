---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 916e818b628608fcae7001797af298317ff96a4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911554"
---
# <span data-ttu-id="80c70-101">Remove-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="80c70-101">Remove-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="80c70-102">簡介</span><span class="sxs-lookup"><span data-stu-id="80c70-102">SYNOPSIS</span></span>
<span data-ttu-id="80c70-103">移除工作區。</span><span class="sxs-lookup"><span data-stu-id="80c70-103">Removes a workspace.</span></span>

## <span data-ttu-id="80c70-104">語法</span><span class="sxs-lookup"><span data-stu-id="80c70-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-ForceDelete] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80c70-105">描述</span><span class="sxs-lookup"><span data-stu-id="80c70-105">DESCRIPTION</span></span>
<span data-ttu-id="80c70-106">**Remove-AzOperationalInsightsWorkspace** Cmdlet 會刪除現有的工作區。</span><span class="sxs-lookup"><span data-stu-id="80c70-106">The **Remove-AzOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="80c70-107">如果此工作區是在建立時透過 *CustomerId* 參數連結至現有帳戶，則原始帳戶不會在營運深入資訊入口網站中刪除。</span><span class="sxs-lookup"><span data-stu-id="80c70-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="80c70-108">例子</span><span class="sxs-lookup"><span data-stu-id="80c70-108">EXAMPLES</span></span>

### <span data-ttu-id="80c70-109">範例 1：根據名稱移除工作區</span><span class="sxs-lookup"><span data-stu-id="80c70-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="80c70-110">此命令會從名為 ContosoResourceGroup 的資源群組移除名為 MyWorkspace 的工作區。</span><span class="sxs-lookup"><span data-stu-id="80c70-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="80c70-111">範例 2：使用管線移除工作區，但不確認</span><span class="sxs-lookup"><span data-stu-id="80c70-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzOperationalInsightsWorkspace -Force
```

<span data-ttu-id="80c70-112">此命令使用 Get-AzOperationalInsightsWorkspace Cmdlet 取得名為 MyWorkspace 的工作區，然後使用管線運算子將其移除，將其傳遞給 **Remove-AzOperationalInsightsWorkspace** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80c70-112">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="80c70-113">由於 *已指定 Force* 參數，因此移除工作區之前，命令不會提示您。</span><span class="sxs-lookup"><span data-stu-id="80c70-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

### <span data-ttu-id="80c70-114">範例 3：強制刪除工作區 (無法復原) </span><span class="sxs-lookup"><span data-stu-id="80c70-114">Example 3: Force delete workspace (cannot be recovered)</span></span>
```
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace -ForceDelete
```

<span data-ttu-id="80c70-115">強制刪除工作區。</span><span class="sxs-lookup"><span data-stu-id="80c70-115">Force delete a workspace.</span></span>

## <span data-ttu-id="80c70-116">參數</span><span class="sxs-lookup"><span data-stu-id="80c70-116">PARAMETERS</span></span>

### <span data-ttu-id="80c70-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80c70-117">-DefaultProfile</span></span>
<span data-ttu-id="80c70-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="80c70-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80c70-119">-強制</span><span class="sxs-lookup"><span data-stu-id="80c70-119">-Force</span></span>
<span data-ttu-id="80c70-120">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="80c70-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="80c70-121">-ForceDelete</span><span class="sxs-lookup"><span data-stu-id="80c70-121">-ForceDelete</span></span>
<span data-ttu-id="80c70-122">強制刪除工作區。</span><span class="sxs-lookup"><span data-stu-id="80c70-122">Force delete workspace.</span></span>

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

### <span data-ttu-id="80c70-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="80c70-123">-Name</span></span>
<span data-ttu-id="80c70-124">指定工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="80c70-124">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="80c70-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80c70-125">-ResourceGroupName</span></span>
<span data-ttu-id="80c70-126">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="80c70-126">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="80c70-127">-確認</span><span class="sxs-lookup"><span data-stu-id="80c70-127">-Confirm</span></span>
<span data-ttu-id="80c70-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="80c70-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80c70-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80c70-129">-WhatIf</span></span>
<span data-ttu-id="80c70-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="80c70-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80c70-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80c70-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80c70-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80c70-132">CommonParameters</span></span>
<span data-ttu-id="80c70-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="80c70-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80c70-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80c70-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80c70-135">輸入</span><span class="sxs-lookup"><span data-stu-id="80c70-135">INPUTS</span></span>

### <span data-ttu-id="80c70-136">System.String</span><span class="sxs-lookup"><span data-stu-id="80c70-136">System.String</span></span>

## <span data-ttu-id="80c70-137">輸出</span><span class="sxs-lookup"><span data-stu-id="80c70-137">OUTPUTS</span></span>

### <span data-ttu-id="80c70-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="80c70-138">System.Void</span></span>

## <span data-ttu-id="80c70-139">筆記</span><span class="sxs-lookup"><span data-stu-id="80c70-139">NOTES</span></span>

## <span data-ttu-id="80c70-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="80c70-140">RELATED LINKS</span></span>

[<span data-ttu-id="80c70-141">Azure 營運深入資訊 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80c70-141">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="80c70-142">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="80c70-142">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


