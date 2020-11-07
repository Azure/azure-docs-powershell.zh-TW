---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
ms.openlocfilehash: 689588e8b92b4b76c97f3972aa63c2f8cdc16535
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794562"
---
# <span data-ttu-id="8cda5-101">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8cda5-101">Remove-AzScheduledQueryRule</span></span>

## <span data-ttu-id="8cda5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8cda5-102">SYNOPSIS</span></span>
<span data-ttu-id="8cda5-103">移除記錄提醒規則</span><span class="sxs-lookup"><span data-stu-id="8cda5-103">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="8cda5-104">句法</span><span class="sxs-lookup"><span data-stu-id="8cda5-104">SYNTAX</span></span>

### <span data-ttu-id="8cda5-105">ByRuleName (預設) </span><span class="sxs-lookup"><span data-stu-id="8cda5-105">ByRuleName (Default)</span></span>
```
Remove-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cda5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8cda5-106">ByInputObject</span></span>
```
Remove-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cda5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8cda5-107">ByResourceId</span></span>
```
Remove-AzScheduledQueryRule -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cda5-108">說明</span><span class="sxs-lookup"><span data-stu-id="8cda5-108">DESCRIPTION</span></span>
<span data-ttu-id="8cda5-109">移除記錄提醒規則</span><span class="sxs-lookup"><span data-stu-id="8cda5-109">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="8cda5-110">示例</span><span class="sxs-lookup"><span data-stu-id="8cda5-110">EXAMPLES</span></span>

### <span data-ttu-id="8cda5-111">範例 1-依規則名稱移除</span><span class="sxs-lookup"><span data-stu-id="8cda5-111">Example 1 - Remove by rule name</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"
```

### <span data-ttu-id="8cda5-112">範例 2-透過輸入物件移除</span><span class="sxs-lookup"><span data-stu-id="8cda5-112">Example 2 - Remove by input object</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -InputObject $PSScheduledQueryRuleResource
```

### <span data-ttu-id="8cda5-113">範例 3-依資源識別碼移除</span><span class="sxs-lookup"><span data-stu-id="8cda5-113">Example 3 - Remove by resource Id</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledQueryRules/LogAlertRule1"
```

## <span data-ttu-id="8cda5-114">參數</span><span class="sxs-lookup"><span data-stu-id="8cda5-114">PARAMETERS</span></span>

### <span data-ttu-id="8cda5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cda5-115">-DefaultProfile</span></span>
<span data-ttu-id="8cda5-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8cda5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cda5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cda5-117">-InputObject</span></span>
<span data-ttu-id="8cda5-118">排程查詢規則資源</span><span class="sxs-lookup"><span data-stu-id="8cda5-118">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="8cda5-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="8cda5-119">-Name</span></span>
<span data-ttu-id="8cda5-120">警示名稱</span><span class="sxs-lookup"><span data-stu-id="8cda5-120">The alert name</span></span>

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

### <span data-ttu-id="8cda5-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8cda5-121">-PassThru</span></span>
<span data-ttu-id="8cda5-122">傳回表示成功或失敗的值。</span><span class="sxs-lookup"><span data-stu-id="8cda5-122">Return a value indicating success or failure.</span></span>
<span data-ttu-id="8cda5-123">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="8cda5-123">This cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8cda5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cda5-124">-ResourceGroupName</span></span>
<span data-ttu-id="8cda5-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="8cda5-125">The resource group name</span></span>

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

### <span data-ttu-id="8cda5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cda5-126">-ResourceId</span></span>
<span data-ttu-id="8cda5-127">資源識別碼</span><span class="sxs-lookup"><span data-stu-id="8cda5-127">The resource Id</span></span>

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

### <span data-ttu-id="8cda5-128">-確認</span><span class="sxs-lookup"><span data-stu-id="8cda5-128">-Confirm</span></span>
<span data-ttu-id="8cda5-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8cda5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cda5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cda5-130">-WhatIf</span></span>
<span data-ttu-id="8cda5-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8cda5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cda5-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8cda5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cda5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cda5-133">CommonParameters</span></span>
<span data-ttu-id="8cda5-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8cda5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cda5-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8cda5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cda5-136">輸入</span><span class="sxs-lookup"><span data-stu-id="8cda5-136">INPUTS</span></span>

### <span data-ttu-id="8cda5-137">PSScheduledQueryRuleResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="8cda5-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="8cda5-138">System.object</span><span class="sxs-lookup"><span data-stu-id="8cda5-138">System.String</span></span>

## <span data-ttu-id="8cda5-139">輸出</span><span class="sxs-lookup"><span data-stu-id="8cda5-139">OUTPUTS</span></span>

### <span data-ttu-id="8cda5-140">System.object</span><span class="sxs-lookup"><span data-stu-id="8cda5-140">System.Boolean</span></span>

## <span data-ttu-id="8cda5-141">筆記</span><span class="sxs-lookup"><span data-stu-id="8cda5-141">NOTES</span></span>

## <span data-ttu-id="8cda5-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="8cda5-142">RELATED LINKS</span></span>
