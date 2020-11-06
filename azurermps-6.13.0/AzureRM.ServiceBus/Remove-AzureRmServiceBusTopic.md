---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
ms.openlocfilehash: 8434893dd3661bbfb1f78a4973dc206f44e9f400
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445452"
---
# <span data-ttu-id="859d0-101">Remove-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="859d0-101">Remove-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="859d0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="859d0-102">SYNOPSIS</span></span>
<span data-ttu-id="859d0-103">從指定的服務匯流排命名空間中移除主題。</span><span class="sxs-lookup"><span data-stu-id="859d0-103">Removes the topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="859d0-104">句法</span><span class="sxs-lookup"><span data-stu-id="859d0-104">SYNTAX</span></span>

### <span data-ttu-id="859d0-105">TopicPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="859d0-105">TopicPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="859d0-106">TopicInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="859d0-106">TopicInputObjectSet</span></span>
```
Remove-AzureRmServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="859d0-107">TopicResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="859d0-107">TopicResourceIdSet</span></span>
```
Remove-AzureRmServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="859d0-108">說明</span><span class="sxs-lookup"><span data-stu-id="859d0-108">DESCRIPTION</span></span>
<span data-ttu-id="859d0-109">**AzureRmServiceBusTopic** Cmdlet 會從指定的服務匯流排命名空間中移除主題。</span><span class="sxs-lookup"><span data-stu-id="859d0-109">The **Remove-AzureRmServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="859d0-110">示例</span><span class="sxs-lookup"><span data-stu-id="859d0-110">EXAMPLES</span></span>

### <span data-ttu-id="859d0-111">範例1</span><span class="sxs-lookup"><span data-stu-id="859d0-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="859d0-112">移除 `SB-Topic_exampl1` 命名空間中的主題 `SB-Example1` 。</span><span class="sxs-lookup"><span data-stu-id="859d0-112">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="859d0-113">範例 2.1-使用變數：</span><span class="sxs-lookup"><span data-stu-id="859d0-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusTopic <parmas>
PS C:\> Remove-AzureRmServiceBusTopic -InputObject $inputobject
```

### <span data-ttu-id="859d0-114">範例 2.2-使用管道的 InputObject：</span><span class="sxs-lookup"><span data-stu-id="859d0-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic <parmas> | Remove-AzureRmServiceBusTopic
```

### <span data-ttu-id="859d0-115">範例 3.1-ResourceId 使用變數：</span><span class="sxs-lookup"><span data-stu-id="859d0-115">Example 3.1 - ResourceId Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzureRmServiceBusTopic <params>
PS C:\> Remove-AzureRmServiceBusTopic -ResourceId $resourceid.Id
```

### <span data-ttu-id="859d0-116">範例 3.2-使用字串值的 ResourceId</span><span class="sxs-lookup"><span data-stu-id="859d0-116">Example 3.2 - ResourceId Using String value</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## <span data-ttu-id="859d0-117">參數</span><span class="sxs-lookup"><span data-stu-id="859d0-117">PARAMETERS</span></span>

### <span data-ttu-id="859d0-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="859d0-118">-AsJob</span></span>
<span data-ttu-id="859d0-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="859d0-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="859d0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="859d0-120">-DefaultProfile</span></span>
<span data-ttu-id="859d0-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="859d0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="859d0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="859d0-122">-InputObject</span></span>
<span data-ttu-id="859d0-123">服務匯流排主題物件</span><span class="sxs-lookup"><span data-stu-id="859d0-123">Service Bus Topic Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: TopicInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="859d0-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="859d0-124">-Name</span></span>
<span data-ttu-id="859d0-125">主題名稱</span><span class="sxs-lookup"><span data-stu-id="859d0-125">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859d0-126">-命名空間</span><span class="sxs-lookup"><span data-stu-id="859d0-126">-Namespace</span></span>
<span data-ttu-id="859d0-127">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="859d0-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859d0-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="859d0-128">-PassThru</span></span>
<span data-ttu-id="859d0-129">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="859d0-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="859d0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="859d0-130">-ResourceGroupName</span></span>
<span data-ttu-id="859d0-131">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="859d0-131">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859d0-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="859d0-132">-ResourceId</span></span>
<span data-ttu-id="859d0-133">服務匯流排主題資源識別碼</span><span class="sxs-lookup"><span data-stu-id="859d0-133">Service Bus Topic Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: TopicResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859d0-134">-確認</span><span class="sxs-lookup"><span data-stu-id="859d0-134">-Confirm</span></span>
<span data-ttu-id="859d0-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="859d0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="859d0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="859d0-136">-WhatIf</span></span>
<span data-ttu-id="859d0-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="859d0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="859d0-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="859d0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="859d0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="859d0-139">CommonParameters</span></span>
<span data-ttu-id="859d0-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="859d0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="859d0-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="859d0-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="859d0-142">輸入</span><span class="sxs-lookup"><span data-stu-id="859d0-142">INPUTS</span></span>

### <span data-ttu-id="859d0-143">System.object</span><span class="sxs-lookup"><span data-stu-id="859d0-143">System.String</span></span>

### <span data-ttu-id="859d0-144">PSTopicAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="859d0-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>
<span data-ttu-id="859d0-145">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="859d0-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="859d0-146">輸出</span><span class="sxs-lookup"><span data-stu-id="859d0-146">OUTPUTS</span></span>

### <span data-ttu-id="859d0-147">System.object</span><span class="sxs-lookup"><span data-stu-id="859d0-147">System.Boolean</span></span>

## <span data-ttu-id="859d0-148">筆記</span><span class="sxs-lookup"><span data-stu-id="859d0-148">NOTES</span></span>

## <span data-ttu-id="859d0-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="859d0-149">RELATED LINKS</span></span>
