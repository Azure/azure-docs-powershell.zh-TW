---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
ms.openlocfilehash: 75da2231dae7ea0dc587d48ca832b7631fc24986
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448359"
---
# <span data-ttu-id="e8276-101">Remove-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="e8276-101">Remove-AzServiceBusTopic</span></span>

## <span data-ttu-id="e8276-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8276-102">SYNOPSIS</span></span>
<span data-ttu-id="e8276-103">從指定的服務匯流排命名空間中移除主題。</span><span class="sxs-lookup"><span data-stu-id="e8276-103">Removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="e8276-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8276-104">SYNTAX</span></span>

### <span data-ttu-id="e8276-105">TopicPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e8276-105">TopicPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8276-106">TopicInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e8276-106">TopicInputObjectSet</span></span>
```
Remove-AzServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8276-107">TopicResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e8276-107">TopicResourceIdSet</span></span>
```
Remove-AzServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8276-108">說明</span><span class="sxs-lookup"><span data-stu-id="e8276-108">DESCRIPTION</span></span>
<span data-ttu-id="e8276-109">**AzServiceBusTopic** Cmdlet 會從指定的服務匯流排命名空間中移除主題。</span><span class="sxs-lookup"><span data-stu-id="e8276-109">The **Remove-AzServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="e8276-110">示例</span><span class="sxs-lookup"><span data-stu-id="e8276-110">EXAMPLES</span></span>

### <span data-ttu-id="e8276-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e8276-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="e8276-112">移除 `SB-Topic_exampl1` 命名空間中的主題 `SB-Example1` 。</span><span class="sxs-lookup"><span data-stu-id="e8276-112">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="e8276-113">範例2：使用 InputObject 的變數：</span><span class="sxs-lookup"><span data-stu-id="e8276-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusTopic <parmas>
PS C:\> Remove-AzServiceBusTopic -InputObject $inputobject
```

### <span data-ttu-id="e8276-114">範例3：使用 [InputObject] 管道：</span><span class="sxs-lookup"><span data-stu-id="e8276-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusTopic <parmas> | Remove-AzServiceBusTopic
```

### <span data-ttu-id="e8276-115">範例4：使用變數的 ResourceId：</span><span class="sxs-lookup"><span data-stu-id="e8276-115">Example 4: ResourceId Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusTopic <params>
PS C:\> Remove-AzServiceBusTopic -ResourceId $resourceid.Id
```

### <span data-ttu-id="e8276-116">範例5：使用字串值的 ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8276-116">Example 5: ResourceId Using String value</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## <span data-ttu-id="e8276-117">參數</span><span class="sxs-lookup"><span data-stu-id="e8276-117">PARAMETERS</span></span>

### <span data-ttu-id="e8276-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8276-118">-AsJob</span></span>
<span data-ttu-id="e8276-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e8276-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e8276-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8276-120">-DefaultProfile</span></span>
<span data-ttu-id="e8276-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8276-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8276-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8276-122">-InputObject</span></span>
<span data-ttu-id="e8276-123">服務匯流排主題物件</span><span class="sxs-lookup"><span data-stu-id="e8276-123">Service Bus Topic Object</span></span>

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

### <span data-ttu-id="e8276-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8276-124">-Name</span></span>
<span data-ttu-id="e8276-125">主題名稱</span><span class="sxs-lookup"><span data-stu-id="e8276-125">Topic Name</span></span>

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

### <span data-ttu-id="e8276-126">-命名空間</span><span class="sxs-lookup"><span data-stu-id="e8276-126">-Namespace</span></span>
<span data-ttu-id="e8276-127">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="e8276-127">Namespace Name</span></span>

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

### <span data-ttu-id="e8276-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8276-128">-PassThru</span></span>
<span data-ttu-id="e8276-129">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="e8276-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="e8276-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8276-130">-ResourceGroupName</span></span>
<span data-ttu-id="e8276-131">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="e8276-131">The name of the resource group</span></span>

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

### <span data-ttu-id="e8276-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8276-132">-ResourceId</span></span>
<span data-ttu-id="e8276-133">服務匯流排主題資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e8276-133">Service Bus Topic Resource Id</span></span>

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

### <span data-ttu-id="e8276-134">-確認</span><span class="sxs-lookup"><span data-stu-id="e8276-134">-Confirm</span></span>
<span data-ttu-id="e8276-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e8276-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8276-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8276-136">-WhatIf</span></span>
<span data-ttu-id="e8276-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e8276-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8276-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8276-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8276-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8276-139">CommonParameters</span></span>
<span data-ttu-id="e8276-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8276-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8276-141">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e8276-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8276-142">輸入</span><span class="sxs-lookup"><span data-stu-id="e8276-142">INPUTS</span></span>

### <span data-ttu-id="e8276-143">System.object</span><span class="sxs-lookup"><span data-stu-id="e8276-143">System.String</span></span>

### <span data-ttu-id="e8276-144">PSTopicAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e8276-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="e8276-145">輸出</span><span class="sxs-lookup"><span data-stu-id="e8276-145">OUTPUTS</span></span>

### <span data-ttu-id="e8276-146">System.object</span><span class="sxs-lookup"><span data-stu-id="e8276-146">System.Boolean</span></span>

## <span data-ttu-id="e8276-147">筆記</span><span class="sxs-lookup"><span data-stu-id="e8276-147">NOTES</span></span>

## <span data-ttu-id="e8276-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8276-148">RELATED LINKS</span></span>
