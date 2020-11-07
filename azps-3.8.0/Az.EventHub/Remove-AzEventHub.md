---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
ms.openlocfilehash: 8dbd46cd3ea5b04c207d0261d4059e557143b1d7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797269"
---
# <span data-ttu-id="a4637-101">Remove-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="a4637-101">Remove-AzEventHub</span></span>

## <span data-ttu-id="a4637-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a4637-102">SYNOPSIS</span></span>
<span data-ttu-id="a4637-103">移除指定的事件中樞。</span><span class="sxs-lookup"><span data-stu-id="a4637-103">Removes the specified Event Hub.</span></span>

## <span data-ttu-id="a4637-104">句法</span><span class="sxs-lookup"><span data-stu-id="a4637-104">SYNTAX</span></span>

### <span data-ttu-id="a4637-105">EventhubDefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a4637-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4637-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a4637-106">EventhubInputObjectSet</span></span>
```
Remove-AzEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4637-107">EventhubResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4637-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4637-108">說明</span><span class="sxs-lookup"><span data-stu-id="a4637-108">DESCRIPTION</span></span>
<span data-ttu-id="a4637-109">Remove-AzEventHub Cmdlet 會從指定的命名空間中移除並刪除指定的事件中樞。</span><span class="sxs-lookup"><span data-stu-id="a4637-109">The Remove-AzEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="a4637-110">示例</span><span class="sxs-lookup"><span data-stu-id="a4637-110">EXAMPLES</span></span>

### <span data-ttu-id="a4637-111">範例1</span><span class="sxs-lookup"><span data-stu-id="a4637-111">Example 1</span></span>
```
PS C:\> Remove-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="a4637-112">移除事件中心 \` MyEventHubName \` 。</span><span class="sxs-lookup"><span data-stu-id="a4637-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="a4637-113">範例 2.1-使用變數：</span><span class="sxs-lookup"><span data-stu-id="a4637-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -InputObject $inputobject
```

### <span data-ttu-id="a4637-114">範例 2.2-InputObject 使用管道：</span><span class="sxs-lookup"><span data-stu-id="a4637-114">Example 2.2 - InputObject Using Piping:</span></span>
```
PS C:\> Get-AzEventHub <params> | Remove-AzEventHub
```

### <span data-ttu-id="a4637-115">範例 3.1-使用變數：</span><span class="sxs-lookup"><span data-stu-id="a4637-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="a4637-116">範例 3.1-使用中字串：</span><span class="sxs-lookup"><span data-stu-id="a4637-116">Example 3.1 - ResourceId - Using string:</span></span>
```
PS C:\> Remove-AzEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="a4637-117">參數</span><span class="sxs-lookup"><span data-stu-id="a4637-117">PARAMETERS</span></span>

### <span data-ttu-id="a4637-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4637-118">-AsJob</span></span>
<span data-ttu-id="a4637-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a4637-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4637-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4637-120">-DefaultProfile</span></span>
<span data-ttu-id="a4637-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a4637-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4637-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4637-122">-InputObject</span></span>
<span data-ttu-id="a4637-123">Eventhub 物件</span><span class="sxs-lookup"><span data-stu-id="a4637-123">Eventhub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4637-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="a4637-124">-Name</span></span>
<span data-ttu-id="a4637-125">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="a4637-125">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4637-126">-命名空間</span><span class="sxs-lookup"><span data-stu-id="a4637-126">-Namespace</span></span>
<span data-ttu-id="a4637-127">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="a4637-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4637-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4637-128">-PassThru</span></span>
<span data-ttu-id="a4637-129">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="a4637-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="a4637-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4637-130">-ResourceGroupName</span></span>
<span data-ttu-id="a4637-131">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="a4637-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4637-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4637-132">-ResourceId</span></span>
<span data-ttu-id="a4637-133">Eventhub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a4637-133">Eventhub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4637-134">-確認</span><span class="sxs-lookup"><span data-stu-id="a4637-134">-Confirm</span></span>
<span data-ttu-id="a4637-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a4637-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4637-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4637-136">-WhatIf</span></span>
<span data-ttu-id="a4637-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a4637-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4637-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a4637-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4637-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4637-139">CommonParameters</span></span>
<span data-ttu-id="a4637-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a4637-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4637-141">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a4637-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4637-142">輸入</span><span class="sxs-lookup"><span data-stu-id="a4637-142">INPUTS</span></span>

### <span data-ttu-id="a4637-143">System.object</span><span class="sxs-lookup"><span data-stu-id="a4637-143">System.String</span></span>

### <span data-ttu-id="a4637-144">PSEventHubAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="a4637-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="a4637-145">輸出</span><span class="sxs-lookup"><span data-stu-id="a4637-145">OUTPUTS</span></span>

### <span data-ttu-id="a4637-146">System.object</span><span class="sxs-lookup"><span data-stu-id="a4637-146">System.Boolean</span></span>

## <span data-ttu-id="a4637-147">筆記</span><span class="sxs-lookup"><span data-stu-id="a4637-147">NOTES</span></span>

## <span data-ttu-id="a4637-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4637-148">RELATED LINKS</span></span>
