---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: dca9094ac66e889b5a00899f6d48d6317279c1fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902902"
---
# <span data-ttu-id="0bbf9-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="0bbf9-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="0bbf9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0bbf9-102">SYNOPSIS</span></span>
<span data-ttu-id="0bbf9-103">移除指定的事件中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="0bbf9-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="0bbf9-104">語法</span><span class="sxs-lookup"><span data-stu-id="0bbf9-104">SYNTAX</span></span>

### <span data-ttu-id="0bbf9-105">命名空間ParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0bbf9-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bbf9-106">命名空間InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0bbf9-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bbf9-107">命名空間ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bbf9-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bbf9-108">描述</span><span class="sxs-lookup"><span data-stu-id="0bbf9-108">DESCRIPTION</span></span>
<span data-ttu-id="0bbf9-109">Cmdlet Remove-AzEventHubNamespace刪除指定的事件中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="0bbf9-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="0bbf9-110">例子</span><span class="sxs-lookup"><span data-stu-id="0bbf9-110">EXAMPLES</span></span>

### <span data-ttu-id="0bbf9-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="0bbf9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="0bbf9-112">移除資源群組 \` MyResourceGroupName 中的事件中樞命名空間 \` \` MyNamespaceName。 \`</span><span class="sxs-lookup"><span data-stu-id="0bbf9-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="0bbf9-113">範例 2：InputObject - Using Variable：</span><span class="sxs-lookup"><span data-stu-id="0bbf9-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="0bbf9-114">範例 3：InputObject - 使用管道：</span><span class="sxs-lookup"><span data-stu-id="0bbf9-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="0bbf9-115">範例 4：ResourceId - Using Variable</span><span class="sxs-lookup"><span data-stu-id="0bbf9-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="0bbf9-116">範例 5：ResourceId - 使用管道：</span><span class="sxs-lookup"><span data-stu-id="0bbf9-116">Example 5: ResourceId - Using Piping:</span></span>
```powershell
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="0bbf9-117">範例 6：ResourceId - 使用字串：</span><span class="sxs-lookup"><span data-stu-id="0bbf9-117">Example 6: ResourceId - Using String:</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="0bbf9-118">參數</span><span class="sxs-lookup"><span data-stu-id="0bbf9-118">PARAMETERS</span></span>

### <span data-ttu-id="0bbf9-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0bbf9-119">-AsJob</span></span>
<span data-ttu-id="0bbf9-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0bbf9-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0bbf9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bbf9-121">-DefaultProfile</span></span>
<span data-ttu-id="0bbf9-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0bbf9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bbf9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0bbf9-123">-InputObject</span></span>
<span data-ttu-id="0bbf9-124">EventHubs 命名空間物件</span><span class="sxs-lookup"><span data-stu-id="0bbf9-124">EventHubs Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0bbf9-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="0bbf9-125">-Name</span></span>
<span data-ttu-id="0bbf9-126">EventHub 命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="0bbf9-126">EventHub Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bbf9-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0bbf9-127">-PassThru</span></span>
<span data-ttu-id="0bbf9-128">如果命令成功，指定此選項會返回 True。</span><span class="sxs-lookup"><span data-stu-id="0bbf9-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="0bbf9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bbf9-129">-ResourceGroupName</span></span>
<span data-ttu-id="0bbf9-130">資源組名</span><span class="sxs-lookup"><span data-stu-id="0bbf9-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bbf9-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bbf9-131">-ResourceId</span></span>
<span data-ttu-id="0bbf9-132">EventHubs 命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="0bbf9-132">EventHubs Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bbf9-133">-確認</span><span class="sxs-lookup"><span data-stu-id="0bbf9-133">-Confirm</span></span>
<span data-ttu-id="0bbf9-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0bbf9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bbf9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bbf9-135">-WhatIf</span></span>
<span data-ttu-id="0bbf9-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0bbf9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bbf9-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0bbf9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bbf9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bbf9-138">CommonParameters</span></span>
<span data-ttu-id="0bbf9-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0bbf9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bbf9-140">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0bbf9-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bbf9-141">輸入</span><span class="sxs-lookup"><span data-stu-id="0bbf9-141">INPUTS</span></span>

### <span data-ttu-id="0bbf9-142">System.String</span><span class="sxs-lookup"><span data-stu-id="0bbf9-142">System.String</span></span>

### <span data-ttu-id="0bbf9-143">Microsoft.Azure.Commands.EventHub.models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="0bbf9-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="0bbf9-144">輸出</span><span class="sxs-lookup"><span data-stu-id="0bbf9-144">OUTPUTS</span></span>

### <span data-ttu-id="0bbf9-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="0bbf9-145">System.Void</span></span>

## <span data-ttu-id="0bbf9-146">筆記</span><span class="sxs-lookup"><span data-stu-id="0bbf9-146">NOTES</span></span>

## <span data-ttu-id="0bbf9-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="0bbf9-147">RELATED LINKS</span></span>
