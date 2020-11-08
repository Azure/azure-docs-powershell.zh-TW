---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: d02338c34584a68ece2ad3a90887a765f8142347
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137832"
---
# <span data-ttu-id="1e28d-101">Remove-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="1e28d-101">Remove-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="1e28d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1e28d-102">SYNOPSIS</span></span>
<span data-ttu-id="1e28d-103">移除工作區。</span><span class="sxs-lookup"><span data-stu-id="1e28d-103">Removes a workspace.</span></span>

## <span data-ttu-id="1e28d-104">句法</span><span class="sxs-lookup"><span data-stu-id="1e28d-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-ForceDelete] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e28d-105">說明</span><span class="sxs-lookup"><span data-stu-id="1e28d-105">DESCRIPTION</span></span>
<span data-ttu-id="1e28d-106">**AzOperationalInsightsWorkspace** Cmdlet 會刪除現有的工作區。</span><span class="sxs-lookup"><span data-stu-id="1e28d-106">The **Remove-AzOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="1e28d-107">如果此工作區是在建立期間透過 [ *CustomerId* ] 參數連結至現有的帳戶，原始帳戶不會在 Operational Insights 入口網站中刪除。</span><span class="sxs-lookup"><span data-stu-id="1e28d-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="1e28d-108">示例</span><span class="sxs-lookup"><span data-stu-id="1e28d-108">EXAMPLES</span></span>

### <span data-ttu-id="1e28d-109">範例1：依名稱移除工作區</span><span class="sxs-lookup"><span data-stu-id="1e28d-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="1e28d-110">這個命令會從名為 ContosoResourceGroup 的資源群組中移除名為 MyWorkspace 的工作區。</span><span class="sxs-lookup"><span data-stu-id="1e28d-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="1e28d-111">範例2：使用管線移除工作區，而不進行確認</span><span class="sxs-lookup"><span data-stu-id="1e28d-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzOperationalInsightsWorkspace -Force
```

<span data-ttu-id="1e28d-112">這個命令會使用 Get-AzOperationalInsightsWorkspace Cmdlet 來取得名為 MyWorkspace 的工作區，然後使用管線運算子將它傳送到 **Remove AzOperationalInsightsWorkspace** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e28d-112">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="1e28d-113">由於已指定 *Force* 參數，因此在移除工作區前，命令不會提示您。</span><span class="sxs-lookup"><span data-stu-id="1e28d-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

### <span data-ttu-id="1e28d-114">範例3：無法復原 [強制刪除工作區] () </span><span class="sxs-lookup"><span data-stu-id="1e28d-114">Example 3: Force delete workspace (cannot be recovered)</span></span>
```
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace -ForceDelete
```

<span data-ttu-id="1e28d-115">強制刪除工作區。</span><span class="sxs-lookup"><span data-stu-id="1e28d-115">Force delete a workspace.</span></span>

## <span data-ttu-id="1e28d-116">參數</span><span class="sxs-lookup"><span data-stu-id="1e28d-116">PARAMETERS</span></span>

### <span data-ttu-id="1e28d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e28d-117">-DefaultProfile</span></span>
<span data-ttu-id="1e28d-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1e28d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e28d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="1e28d-119">-Force</span></span>
<span data-ttu-id="1e28d-120">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="1e28d-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1e28d-121">-ForceDelete</span><span class="sxs-lookup"><span data-stu-id="1e28d-121">-ForceDelete</span></span>
<span data-ttu-id="1e28d-122">強制刪除工作區。</span><span class="sxs-lookup"><span data-stu-id="1e28d-122">Force delete workspace.</span></span>

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

### <span data-ttu-id="1e28d-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="1e28d-123">-Name</span></span>
<span data-ttu-id="1e28d-124">指定工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e28d-124">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="1e28d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e28d-125">-ResourceGroupName</span></span>
<span data-ttu-id="1e28d-126">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e28d-126">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="1e28d-127">-確認</span><span class="sxs-lookup"><span data-stu-id="1e28d-127">-Confirm</span></span>
<span data-ttu-id="1e28d-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1e28d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e28d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e28d-129">-WhatIf</span></span>
<span data-ttu-id="1e28d-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1e28d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e28d-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e28d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e28d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e28d-132">CommonParameters</span></span>
<span data-ttu-id="1e28d-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1e28d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e28d-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1e28d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e28d-135">輸入</span><span class="sxs-lookup"><span data-stu-id="1e28d-135">INPUTS</span></span>

### <span data-ttu-id="1e28d-136">System.object</span><span class="sxs-lookup"><span data-stu-id="1e28d-136">System.String</span></span>

## <span data-ttu-id="1e28d-137">輸出</span><span class="sxs-lookup"><span data-stu-id="1e28d-137">OUTPUTS</span></span>

### <span data-ttu-id="1e28d-138">System.void</span><span class="sxs-lookup"><span data-stu-id="1e28d-138">System.Void</span></span>

## <span data-ttu-id="1e28d-139">筆記</span><span class="sxs-lookup"><span data-stu-id="1e28d-139">NOTES</span></span>

## <span data-ttu-id="1e28d-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e28d-140">RELATED LINKS</span></span>

[<span data-ttu-id="1e28d-141">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1e28d-141">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="1e28d-142">AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="1e28d-142">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


