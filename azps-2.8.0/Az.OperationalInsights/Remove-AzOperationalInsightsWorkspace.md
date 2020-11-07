---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 9758c0dda8d392100e57909edca310f14d3746af
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93799358"
---
# <span data-ttu-id="c7649-101">Remove-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="c7649-101">Remove-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="c7649-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c7649-102">SYNOPSIS</span></span>
<span data-ttu-id="c7649-103">移除工作區。</span><span class="sxs-lookup"><span data-stu-id="c7649-103">Removes a workspace.</span></span>

## <span data-ttu-id="c7649-104">句法</span><span class="sxs-lookup"><span data-stu-id="c7649-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7649-105">說明</span><span class="sxs-lookup"><span data-stu-id="c7649-105">DESCRIPTION</span></span>
<span data-ttu-id="c7649-106">**AzOperationalInsightsWorkspace** Cmdlet 會刪除現有的工作區。</span><span class="sxs-lookup"><span data-stu-id="c7649-106">The **Remove-AzOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="c7649-107">如果此工作區是在建立期間透過 [ *CustomerId* ] 參數連結至現有的帳戶，原始帳戶不會在 Operational Insights 入口網站中刪除。</span><span class="sxs-lookup"><span data-stu-id="c7649-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="c7649-108">示例</span><span class="sxs-lookup"><span data-stu-id="c7649-108">EXAMPLES</span></span>

### <span data-ttu-id="c7649-109">範例1：依名稱移除工作區</span><span class="sxs-lookup"><span data-stu-id="c7649-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="c7649-110">這個命令會從名為 ContosoResourceGroup 的資源群組中移除名為 MyWorkspace 的工作區。</span><span class="sxs-lookup"><span data-stu-id="c7649-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="c7649-111">範例2：使用管線移除工作區，而不進行確認</span><span class="sxs-lookup"><span data-stu-id="c7649-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzOperationalInsightsWorkspace -Force
```

<span data-ttu-id="c7649-112">這個命令會使用 Get-AzOperationalInsightsWorkspace Cmdlet 來取得名為 MyWorkspace 的工作區，然後使用管線運算子將它傳送到 **Remove AzOperationalInsightsWorkspace** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c7649-112">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="c7649-113">由於已指定 *Force* 參數，因此在移除工作區前，命令不會提示您。</span><span class="sxs-lookup"><span data-stu-id="c7649-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

## <span data-ttu-id="c7649-114">參數</span><span class="sxs-lookup"><span data-stu-id="c7649-114">PARAMETERS</span></span>

### <span data-ttu-id="c7649-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7649-115">-DefaultProfile</span></span>
<span data-ttu-id="c7649-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c7649-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7649-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c7649-117">-Force</span></span>
<span data-ttu-id="c7649-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="c7649-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c7649-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="c7649-119">-Name</span></span>
<span data-ttu-id="c7649-120">指定工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="c7649-120">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="c7649-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7649-121">-ResourceGroupName</span></span>
<span data-ttu-id="c7649-122">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c7649-122">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="c7649-123">-確認</span><span class="sxs-lookup"><span data-stu-id="c7649-123">-Confirm</span></span>
<span data-ttu-id="c7649-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c7649-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7649-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7649-125">-WhatIf</span></span>
<span data-ttu-id="c7649-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c7649-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7649-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c7649-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7649-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7649-128">CommonParameters</span></span>
<span data-ttu-id="c7649-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c7649-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7649-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c7649-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7649-131">輸入</span><span class="sxs-lookup"><span data-stu-id="c7649-131">INPUTS</span></span>

### <span data-ttu-id="c7649-132">System.object</span><span class="sxs-lookup"><span data-stu-id="c7649-132">System.String</span></span>

## <span data-ttu-id="c7649-133">輸出</span><span class="sxs-lookup"><span data-stu-id="c7649-133">OUTPUTS</span></span>

### <span data-ttu-id="c7649-134">System.void</span><span class="sxs-lookup"><span data-stu-id="c7649-134">System.Void</span></span>

## <span data-ttu-id="c7649-135">筆記</span><span class="sxs-lookup"><span data-stu-id="c7649-135">NOTES</span></span>

## <span data-ttu-id="c7649-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7649-136">RELATED LINKS</span></span>

[<span data-ttu-id="c7649-137">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c7649-137">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="c7649-138">AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="c7649-138">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


