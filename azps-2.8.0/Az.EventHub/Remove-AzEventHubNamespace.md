---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: 4d5ddbc4dff2922b90bc6d1117ff32473afd9042
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612405"
---
# <span data-ttu-id="3c772-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="3c772-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="3c772-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3c772-102">SYNOPSIS</span></span>
<span data-ttu-id="3c772-103">移除指定的事件中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="3c772-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="3c772-104">句法</span><span class="sxs-lookup"><span data-stu-id="3c772-104">SYNTAX</span></span>

### <span data-ttu-id="3c772-105">NamespaceParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3c772-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c772-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3c772-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c772-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c772-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c772-108">說明</span><span class="sxs-lookup"><span data-stu-id="3c772-108">DESCRIPTION</span></span>
<span data-ttu-id="3c772-109">Remove-AzEventHubNamespace Cmdlet 會移除並刪除指定的事件中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="3c772-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="3c772-110">示例</span><span class="sxs-lookup"><span data-stu-id="3c772-110">EXAMPLES</span></span>

### <span data-ttu-id="3c772-111">範例1</span><span class="sxs-lookup"><span data-stu-id="3c772-111">Example 1</span></span>
```
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="3c772-112">移除 \` \` 資源群組 MyResourceGroupName 中的 [事件中心] 命名空間 MyNamespaceName \` \` 。</span><span class="sxs-lookup"><span data-stu-id="3c772-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="3c772-113">範例 2.1-使用變數：</span><span class="sxs-lookup"><span data-stu-id="3c772-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="3c772-114">範例 2.1-使用管道的 InputObject：</span><span class="sxs-lookup"><span data-stu-id="3c772-114">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="3c772-115">範例 3.1-使用變數的 ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c772-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="3c772-116">範例 3.2-使用管道的作業 Id：</span><span class="sxs-lookup"><span data-stu-id="3c772-116">Example 3.2 - ResourceId - Using Piping:</span></span>
```
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="3c772-117">範例 3.3-使用中字串：</span><span class="sxs-lookup"><span data-stu-id="3c772-117">Example 3.3 - ResourceId - Using String:</span></span>
```
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="3c772-118">參數</span><span class="sxs-lookup"><span data-stu-id="3c772-118">PARAMETERS</span></span>

### <span data-ttu-id="3c772-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c772-119">-AsJob</span></span>
<span data-ttu-id="3c772-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3c772-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c772-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c772-121">-DefaultProfile</span></span>
<span data-ttu-id="3c772-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3c772-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c772-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c772-123">-InputObject</span></span>
<span data-ttu-id="3c772-124">EventHubs Namespace 物件</span><span class="sxs-lookup"><span data-stu-id="3c772-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="3c772-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="3c772-125">-Name</span></span>
<span data-ttu-id="3c772-126">EventHub 命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="3c772-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="3c772-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c772-127">-PassThru</span></span>
<span data-ttu-id="3c772-128">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="3c772-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="3c772-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c772-129">-ResourceGroupName</span></span>
<span data-ttu-id="3c772-130">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="3c772-130">Resource Group Name</span></span>

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

### <span data-ttu-id="3c772-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c772-131">-ResourceId</span></span>
<span data-ttu-id="3c772-132">EventHubs 命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="3c772-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="3c772-133">-確認</span><span class="sxs-lookup"><span data-stu-id="3c772-133">-Confirm</span></span>
<span data-ttu-id="3c772-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3c772-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c772-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c772-135">-WhatIf</span></span>
<span data-ttu-id="3c772-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3c772-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c772-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3c772-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c772-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c772-138">CommonParameters</span></span>
<span data-ttu-id="3c772-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3c772-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c772-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3c772-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c772-141">輸入</span><span class="sxs-lookup"><span data-stu-id="3c772-141">INPUTS</span></span>

### <span data-ttu-id="3c772-142">System.object</span><span class="sxs-lookup"><span data-stu-id="3c772-142">System.String</span></span>

### <span data-ttu-id="3c772-143">PSNamespaceAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="3c772-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="3c772-144">輸出</span><span class="sxs-lookup"><span data-stu-id="3c772-144">OUTPUTS</span></span>

### <span data-ttu-id="3c772-145">System.void</span><span class="sxs-lookup"><span data-stu-id="3c772-145">System.Void</span></span>

## <span data-ttu-id="3c772-146">筆記</span><span class="sxs-lookup"><span data-stu-id="3c772-146">NOTES</span></span>

## <span data-ttu-id="3c772-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="3c772-147">RELATED LINKS</span></span>
