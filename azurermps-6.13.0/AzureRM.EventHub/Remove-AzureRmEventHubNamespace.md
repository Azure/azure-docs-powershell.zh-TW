---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
ms.openlocfilehash: 6df8d5539bf340df5e00ad69ac557bc2cbb8ccaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449182"
---
# <span data-ttu-id="1657d-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="1657d-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="1657d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1657d-102">SYNOPSIS</span></span>
<span data-ttu-id="1657d-103">移除指定的事件中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="1657d-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1657d-104">句法</span><span class="sxs-lookup"><span data-stu-id="1657d-104">SYNTAX</span></span>

### <span data-ttu-id="1657d-105">NamespaceParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1657d-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1657d-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1657d-106">NamespaceInputObjectSet</span></span>
```
Remove-AzureRmEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1657d-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1657d-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1657d-108">說明</span><span class="sxs-lookup"><span data-stu-id="1657d-108">DESCRIPTION</span></span>
<span data-ttu-id="1657d-109">Remove-AzureRmEventHubNamespace Cmdlet 會移除並刪除指定的事件中樞命名空間。</span><span class="sxs-lookup"><span data-stu-id="1657d-109">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="1657d-110">示例</span><span class="sxs-lookup"><span data-stu-id="1657d-110">EXAMPLES</span></span>

### <span data-ttu-id="1657d-111">範例1</span><span class="sxs-lookup"><span data-stu-id="1657d-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="1657d-112">移除 \` \` 資源群組 MyResourceGroupName 中的 [事件中心] 命名空間 MyNamespaceName \` \` 。</span><span class="sxs-lookup"><span data-stu-id="1657d-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="1657d-113">範例 2.1-使用變數：</span><span class="sxs-lookup"><span data-stu-id="1657d-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputObject = Get-AzureRmEventHubNamespace <params> 
PS C:\> Remove-AzureRmEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="1657d-114">範例 2.1-使用管道的 InputObject：</span><span class="sxs-lookup"><span data-stu-id="1657d-114">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace <params> | Remove-AzureRmEventHubNamespace
```

### <span data-ttu-id="1657d-115">範例 3.1-使用變數的 ResourceId</span><span class="sxs-lookup"><span data-stu-id="1657d-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzureRmEventHubNamespace <params>
PS C:\> Remove-AzureRmEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="1657d-116">範例 3.2-使用管道的作業 Id：</span><span class="sxs-lookup"><span data-stu-id="1657d-116">Example 3.2 - ResourceId - Using Piping:</span></span>
```
PS C:\> Get-AzureRmResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzureRmEventHubNamespace
```

### <span data-ttu-id="1657d-117">範例 3.3-使用中字串：</span><span class="sxs-lookup"><span data-stu-id="1657d-117">Example 3.3 - ResourceId - Using String:</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="1657d-118">參數</span><span class="sxs-lookup"><span data-stu-id="1657d-118">PARAMETERS</span></span>

### <span data-ttu-id="1657d-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1657d-119">-AsJob</span></span>
<span data-ttu-id="1657d-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1657d-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1657d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1657d-121">-DefaultProfile</span></span>
<span data-ttu-id="1657d-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1657d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1657d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1657d-123">-InputObject</span></span>
<span data-ttu-id="1657d-124">EventHubs Namespace 物件</span><span class="sxs-lookup"><span data-stu-id="1657d-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="1657d-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="1657d-125">-Name</span></span>
<span data-ttu-id="1657d-126">EventHub 命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="1657d-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="1657d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1657d-127">-PassThru</span></span>
<span data-ttu-id="1657d-128">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="1657d-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="1657d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1657d-129">-ResourceGroupName</span></span>
<span data-ttu-id="1657d-130">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="1657d-130">Resource Group Name</span></span>

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

### <span data-ttu-id="1657d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1657d-131">-ResourceId</span></span>
<span data-ttu-id="1657d-132">EventHubs 命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="1657d-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="1657d-133">-確認</span><span class="sxs-lookup"><span data-stu-id="1657d-133">-Confirm</span></span>
<span data-ttu-id="1657d-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1657d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1657d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1657d-135">-WhatIf</span></span>
<span data-ttu-id="1657d-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1657d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1657d-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1657d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1657d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1657d-138">CommonParameters</span></span>
<span data-ttu-id="1657d-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1657d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1657d-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1657d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1657d-141">輸入</span><span class="sxs-lookup"><span data-stu-id="1657d-141">INPUTS</span></span>

### <span data-ttu-id="1657d-142">System.object</span><span class="sxs-lookup"><span data-stu-id="1657d-142">System.String</span></span>

### <span data-ttu-id="1657d-143">PSNamespaceAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="1657d-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="1657d-144">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="1657d-144">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="1657d-145">輸出</span><span class="sxs-lookup"><span data-stu-id="1657d-145">OUTPUTS</span></span>

### <span data-ttu-id="1657d-146">System.void</span><span class="sxs-lookup"><span data-stu-id="1657d-146">System.Void</span></span>

## <span data-ttu-id="1657d-147">筆記</span><span class="sxs-lookup"><span data-stu-id="1657d-147">NOTES</span></span>

## <span data-ttu-id="1657d-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="1657d-148">RELATED LINKS</span></span>
