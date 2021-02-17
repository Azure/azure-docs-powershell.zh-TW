---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
ms.openlocfilehash: ea7679b2e3214c55463f9f6fd4ccaf2b22d32841
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140599"
---
# <span data-ttu-id="1681c-101">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1681c-101">Remove-AzScheduledQueryRule</span></span>

## <span data-ttu-id="1681c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1681c-102">SYNOPSIS</span></span>
<span data-ttu-id="1681c-103">移除記錄提醒規則</span><span class="sxs-lookup"><span data-stu-id="1681c-103">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="1681c-104">句法</span><span class="sxs-lookup"><span data-stu-id="1681c-104">SYNTAX</span></span>

### <span data-ttu-id="1681c-105">ByRuleName (預設) </span><span class="sxs-lookup"><span data-stu-id="1681c-105">ByRuleName (Default)</span></span>
```
Remove-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1681c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1681c-106">ByInputObject</span></span>
```
Remove-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1681c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1681c-107">ByResourceId</span></span>
```
Remove-AzScheduledQueryRule -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1681c-108">說明</span><span class="sxs-lookup"><span data-stu-id="1681c-108">DESCRIPTION</span></span>
<span data-ttu-id="1681c-109">移除記錄提醒規則</span><span class="sxs-lookup"><span data-stu-id="1681c-109">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="1681c-110">示例</span><span class="sxs-lookup"><span data-stu-id="1681c-110">EXAMPLES</span></span>

### <span data-ttu-id="1681c-111">範例1：依規則名稱移除</span><span class="sxs-lookup"><span data-stu-id="1681c-111">Example 1: Remove by rule name</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"
```

### <span data-ttu-id="1681c-112">範例2：移除輸入物件</span><span class="sxs-lookup"><span data-stu-id="1681c-112">Example 2: Remove by input object</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -InputObject $PSScheduledQueryRuleResource
```

### <span data-ttu-id="1681c-113">範例3：依資源識別碼移除</span><span class="sxs-lookup"><span data-stu-id="1681c-113">Example 3: Remove by resource Id</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledQueryRules/LogAlertRule1"
```

## <span data-ttu-id="1681c-114">參數</span><span class="sxs-lookup"><span data-stu-id="1681c-114">PARAMETERS</span></span>

### <span data-ttu-id="1681c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1681c-115">-DefaultProfile</span></span>
<span data-ttu-id="1681c-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1681c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1681c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1681c-117">-InputObject</span></span>
<span data-ttu-id="1681c-118">排程查詢規則資源</span><span class="sxs-lookup"><span data-stu-id="1681c-118">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="1681c-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="1681c-119">-Name</span></span>
<span data-ttu-id="1681c-120">警示名稱</span><span class="sxs-lookup"><span data-stu-id="1681c-120">The alert name</span></span>

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

### <span data-ttu-id="1681c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1681c-121">-PassThru</span></span>
<span data-ttu-id="1681c-122">傳回表示成功或失敗的值。</span><span class="sxs-lookup"><span data-stu-id="1681c-122">Return a value indicating success or failure.</span></span>
<span data-ttu-id="1681c-123">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="1681c-123">This cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1681c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1681c-124">-ResourceGroupName</span></span>
<span data-ttu-id="1681c-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="1681c-125">The resource group name</span></span>

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

### <span data-ttu-id="1681c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1681c-126">-ResourceId</span></span>
<span data-ttu-id="1681c-127">資源識別碼</span><span class="sxs-lookup"><span data-stu-id="1681c-127">The resource Id</span></span>

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

### <span data-ttu-id="1681c-128">-確認</span><span class="sxs-lookup"><span data-stu-id="1681c-128">-Confirm</span></span>
<span data-ttu-id="1681c-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1681c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1681c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1681c-130">-WhatIf</span></span>
<span data-ttu-id="1681c-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1681c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1681c-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1681c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1681c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1681c-133">CommonParameters</span></span>
<span data-ttu-id="1681c-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1681c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1681c-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1681c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1681c-136">輸入</span><span class="sxs-lookup"><span data-stu-id="1681c-136">INPUTS</span></span>

### <span data-ttu-id="1681c-137">PSScheduledQueryRuleResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="1681c-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="1681c-138">System.object</span><span class="sxs-lookup"><span data-stu-id="1681c-138">System.String</span></span>

## <span data-ttu-id="1681c-139">輸出</span><span class="sxs-lookup"><span data-stu-id="1681c-139">OUTPUTS</span></span>

### <span data-ttu-id="1681c-140">System.object</span><span class="sxs-lookup"><span data-stu-id="1681c-140">System.Boolean</span></span>

## <span data-ttu-id="1681c-141">筆記</span><span class="sxs-lookup"><span data-stu-id="1681c-141">NOTES</span></span>

## <span data-ttu-id="1681c-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="1681c-142">RELATED LINKS</span></span>
