---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/restore-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 1035d918870a15000be066fd59cc72913d8d8cf5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911553"
---
# <span data-ttu-id="83e9f-101">Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="83e9f-101">Restore-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="83e9f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="83e9f-102">SYNOPSIS</span></span>
<span data-ttu-id="83e9f-103">還原已刪除的工作區。</span><span class="sxs-lookup"><span data-stu-id="83e9f-103">Restore a deleted workspace.</span></span>

## <span data-ttu-id="83e9f-104">語法</span><span class="sxs-lookup"><span data-stu-id="83e9f-104">SYNTAX</span></span>

```
Restore-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83e9f-105">描述</span><span class="sxs-lookup"><span data-stu-id="83e9f-105">DESCRIPTION</span></span>
<span data-ttu-id="83e9f-106">還原已刪除的工作區。</span><span class="sxs-lookup"><span data-stu-id="83e9f-106">Restore a deleted workspace.</span></span>

## <span data-ttu-id="83e9f-107">例子</span><span class="sxs-lookup"><span data-stu-id="83e9f-107">EXAMPLES</span></span>

### <span data-ttu-id="83e9f-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="83e9f-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> $workspace = Restore-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
```

<span data-ttu-id="83e9f-109">還原已刪除的工作區。</span><span class="sxs-lookup"><span data-stu-id="83e9f-109">Restore deleted workspace.</span></span>

## <span data-ttu-id="83e9f-110">參數</span><span class="sxs-lookup"><span data-stu-id="83e9f-110">PARAMETERS</span></span>

### <span data-ttu-id="83e9f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83e9f-111">-DefaultProfile</span></span>
<span data-ttu-id="83e9f-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="83e9f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83e9f-113">-強制</span><span class="sxs-lookup"><span data-stu-id="83e9f-113">-Force</span></span>
<span data-ttu-id="83e9f-114">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="83e9f-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="83e9f-115">-位置</span><span class="sxs-lookup"><span data-stu-id="83e9f-115">-Location</span></span>
<span data-ttu-id="83e9f-116">建立工作區的地理區域。</span><span class="sxs-lookup"><span data-stu-id="83e9f-116">The geographic region that the workspace will be created in.</span></span>

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

### <span data-ttu-id="83e9f-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="83e9f-117">-Name</span></span>
<span data-ttu-id="83e9f-118">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="83e9f-118">The workspace name.</span></span>

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

### <span data-ttu-id="83e9f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83e9f-119">-ResourceGroupName</span></span>
<span data-ttu-id="83e9f-120">資源組名。</span><span class="sxs-lookup"><span data-stu-id="83e9f-120">The resource group name.</span></span>

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

### <span data-ttu-id="83e9f-121">-確認</span><span class="sxs-lookup"><span data-stu-id="83e9f-121">-Confirm</span></span>
<span data-ttu-id="83e9f-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="83e9f-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e9f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83e9f-123">-WhatIf</span></span>
<span data-ttu-id="83e9f-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="83e9f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83e9f-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="83e9f-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e9f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83e9f-126">CommonParameters</span></span>
<span data-ttu-id="83e9f-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="83e9f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83e9f-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83e9f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83e9f-129">輸入</span><span class="sxs-lookup"><span data-stu-id="83e9f-129">INPUTS</span></span>

### <span data-ttu-id="83e9f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="83e9f-130">System.String</span></span>

## <span data-ttu-id="83e9f-131">輸出</span><span class="sxs-lookup"><span data-stu-id="83e9f-131">OUTPUTS</span></span>

### <span data-ttu-id="83e9f-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="83e9f-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="83e9f-133">筆記</span><span class="sxs-lookup"><span data-stu-id="83e9f-133">NOTES</span></span>

## <span data-ttu-id="83e9f-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="83e9f-134">RELATED LINKS</span></span>
