---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
ms.openlocfilehash: 24ad63f1422a829a0cef3ed0c4907ea5687b6151
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912381"
---
# <span data-ttu-id="cf711-101">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cf711-101">Remove-AzScheduledQueryRule</span></span>

## <span data-ttu-id="cf711-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cf711-102">SYNOPSIS</span></span>
<span data-ttu-id="cf711-103">移除記錄提醒規則</span><span class="sxs-lookup"><span data-stu-id="cf711-103">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="cf711-104">語法</span><span class="sxs-lookup"><span data-stu-id="cf711-104">SYNTAX</span></span>

### <span data-ttu-id="cf711-105">ByRuleName (預設) </span><span class="sxs-lookup"><span data-stu-id="cf711-105">ByRuleName (Default)</span></span>
```
Remove-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf711-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cf711-106">ByInputObject</span></span>
```
Remove-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf711-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cf711-107">ByResourceId</span></span>
```
Remove-AzScheduledQueryRule -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf711-108">描述</span><span class="sxs-lookup"><span data-stu-id="cf711-108">DESCRIPTION</span></span>
<span data-ttu-id="cf711-109">移除記錄提醒規則</span><span class="sxs-lookup"><span data-stu-id="cf711-109">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="cf711-110">例子</span><span class="sxs-lookup"><span data-stu-id="cf711-110">EXAMPLES</span></span>

### <span data-ttu-id="cf711-111">範例 1：依規則名稱移除</span><span class="sxs-lookup"><span data-stu-id="cf711-111">Example 1: Remove by rule name</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"
```

### <span data-ttu-id="cf711-112">範例 2：根據輸入物件移除</span><span class="sxs-lookup"><span data-stu-id="cf711-112">Example 2: Remove by input object</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -InputObject $PSScheduledQueryRuleResource
```

### <span data-ttu-id="cf711-113">範例 3：根據資源識別碼移除</span><span class="sxs-lookup"><span data-stu-id="cf711-113">Example 3: Remove by resource Id</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledQueryRules/LogAlertRule1"
```

## <span data-ttu-id="cf711-114">參數</span><span class="sxs-lookup"><span data-stu-id="cf711-114">PARAMETERS</span></span>

### <span data-ttu-id="cf711-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf711-115">-DefaultProfile</span></span>
<span data-ttu-id="cf711-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf711-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf711-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf711-117">-InputObject</span></span>
<span data-ttu-id="cf711-118">排程查詢規則資源</span><span class="sxs-lookup"><span data-stu-id="cf711-118">The Scheduled Query Rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf711-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="cf711-119">-Name</span></span>
<span data-ttu-id="cf711-120">警示名稱</span><span class="sxs-lookup"><span data-stu-id="cf711-120">The alert name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf711-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf711-121">-PassThru</span></span>
<span data-ttu-id="cf711-122">會返回指出成功或失敗的值。</span><span class="sxs-lookup"><span data-stu-id="cf711-122">Return a value indicating success or failure.</span></span>
<span data-ttu-id="cf711-123">此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="cf711-123">This cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cf711-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf711-124">-ResourceGroupName</span></span>
<span data-ttu-id="cf711-125">資源組名</span><span class="sxs-lookup"><span data-stu-id="cf711-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf711-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf711-126">-ResourceId</span></span>
<span data-ttu-id="cf711-127">資源識別碼</span><span class="sxs-lookup"><span data-stu-id="cf711-127">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf711-128">-確認</span><span class="sxs-lookup"><span data-stu-id="cf711-128">-Confirm</span></span>
<span data-ttu-id="cf711-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cf711-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf711-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf711-130">-WhatIf</span></span>
<span data-ttu-id="cf711-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cf711-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf711-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf711-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf711-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf711-133">CommonParameters</span></span>
<span data-ttu-id="cf711-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cf711-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf711-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf711-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf711-136">輸入</span><span class="sxs-lookup"><span data-stu-id="cf711-136">INPUTS</span></span>

### <span data-ttu-id="cf711-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="cf711-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="cf711-138">System.String</span><span class="sxs-lookup"><span data-stu-id="cf711-138">System.String</span></span>

## <span data-ttu-id="cf711-139">輸出</span><span class="sxs-lookup"><span data-stu-id="cf711-139">OUTPUTS</span></span>

### <span data-ttu-id="cf711-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cf711-140">System.Boolean</span></span>

## <span data-ttu-id="cf711-141">筆記</span><span class="sxs-lookup"><span data-stu-id="cf711-141">NOTES</span></span>

## <span data-ttu-id="cf711-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf711-142">RELATED LINKS</span></span>
