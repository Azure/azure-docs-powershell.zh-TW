---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
ms.openlocfilehash: 2d3f2ee9a4dc55dd709be3113770df402434c911
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912418"
---
# <span data-ttu-id="7b72e-101">Remove-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="7b72e-101">Remove-AzEventHub</span></span>

## <span data-ttu-id="7b72e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7b72e-102">SYNOPSIS</span></span>
<span data-ttu-id="7b72e-103">移除指定的事件中樞。</span><span class="sxs-lookup"><span data-stu-id="7b72e-103">Removes the specified Event Hub.</span></span>

## <span data-ttu-id="7b72e-104">語法</span><span class="sxs-lookup"><span data-stu-id="7b72e-104">SYNTAX</span></span>

### <span data-ttu-id="7b72e-105">EventhubDefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7b72e-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b72e-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7b72e-106">EventhubInputObjectSet</span></span>
```
Remove-AzEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b72e-107">EventhubResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b72e-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b72e-108">描述</span><span class="sxs-lookup"><span data-stu-id="7b72e-108">DESCRIPTION</span></span>
<span data-ttu-id="7b72e-109">此Remove-AzEventHub Cmdlet 會從指定的命名空間移除及刪除指定的事件中樞。</span><span class="sxs-lookup"><span data-stu-id="7b72e-109">The Remove-AzEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="7b72e-110">例子</span><span class="sxs-lookup"><span data-stu-id="7b72e-110">EXAMPLES</span></span>

### <span data-ttu-id="7b72e-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="7b72e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="7b72e-112">移除事件中樞 \` MyEventHubName。 \`</span><span class="sxs-lookup"><span data-stu-id="7b72e-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="7b72e-113">範例 2：InputObject - Using Variable：</span><span class="sxs-lookup"><span data-stu-id="7b72e-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -InputObject $inputobject
```

### <span data-ttu-id="7b72e-114">範例 3：InputObject Using Piping：</span><span class="sxs-lookup"><span data-stu-id="7b72e-114">Example 3: InputObject Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHub <params> | Remove-AzEventHub
```

### <span data-ttu-id="7b72e-115">範例 4：ResourceId - Using Variable：</span><span class="sxs-lookup"><span data-stu-id="7b72e-115">Example 4: ResourceId - Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="7b72e-116">範例 5：ResourceId - 使用字串：</span><span class="sxs-lookup"><span data-stu-id="7b72e-116">Example 5: ResourceId - Using string:</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="7b72e-117">參數</span><span class="sxs-lookup"><span data-stu-id="7b72e-117">PARAMETERS</span></span>

### <span data-ttu-id="7b72e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b72e-118">-AsJob</span></span>
<span data-ttu-id="7b72e-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7b72e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b72e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b72e-120">-DefaultProfile</span></span>
<span data-ttu-id="7b72e-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7b72e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b72e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b72e-122">-InputObject</span></span>
<span data-ttu-id="7b72e-123">Eventhub 物件</span><span class="sxs-lookup"><span data-stu-id="7b72e-123">Eventhub Object</span></span>

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

### <span data-ttu-id="7b72e-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="7b72e-124">-Name</span></span>
<span data-ttu-id="7b72e-125">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="7b72e-125">EventHub Name</span></span>

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

### <span data-ttu-id="7b72e-126">-命名空間</span><span class="sxs-lookup"><span data-stu-id="7b72e-126">-Namespace</span></span>
<span data-ttu-id="7b72e-127">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="7b72e-127">Namespace Name</span></span>

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

### <span data-ttu-id="7b72e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b72e-128">-PassThru</span></span>
<span data-ttu-id="7b72e-129">如果命令成功，指定此選項會返回 True。</span><span class="sxs-lookup"><span data-stu-id="7b72e-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="7b72e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b72e-130">-ResourceGroupName</span></span>
<span data-ttu-id="7b72e-131">資源組名</span><span class="sxs-lookup"><span data-stu-id="7b72e-131">Resource Group Name</span></span>

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

### <span data-ttu-id="7b72e-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b72e-132">-ResourceId</span></span>
<span data-ttu-id="7b72e-133">Eventhub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="7b72e-133">Eventhub Resource Id</span></span>

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

### <span data-ttu-id="7b72e-134">-確認</span><span class="sxs-lookup"><span data-stu-id="7b72e-134">-Confirm</span></span>
<span data-ttu-id="7b72e-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7b72e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b72e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b72e-136">-WhatIf</span></span>
<span data-ttu-id="7b72e-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7b72e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b72e-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7b72e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b72e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b72e-139">CommonParameters</span></span>
<span data-ttu-id="7b72e-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7b72e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b72e-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="7b72e-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b72e-142">輸入</span><span class="sxs-lookup"><span data-stu-id="7b72e-142">INPUTS</span></span>

### <span data-ttu-id="7b72e-143">System.String</span><span class="sxs-lookup"><span data-stu-id="7b72e-143">System.String</span></span>

### <span data-ttu-id="7b72e-144">Microsoft.Azure.Commands.EventHub.models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="7b72e-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="7b72e-145">輸出</span><span class="sxs-lookup"><span data-stu-id="7b72e-145">OUTPUTS</span></span>

### <span data-ttu-id="7b72e-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7b72e-146">System.Boolean</span></span>

## <span data-ttu-id="7b72e-147">筆記</span><span class="sxs-lookup"><span data-stu-id="7b72e-147">NOTES</span></span>

## <span data-ttu-id="7b72e-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="7b72e-148">RELATED LINKS</span></span>
