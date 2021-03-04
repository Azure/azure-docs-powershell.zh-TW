---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
ms.openlocfilehash: 445108b2413673e2ce48dcbfac9f3fa0cdb45982
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912581"
---
# <span data-ttu-id="11ee1-101">Remove-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="11ee1-101">Remove-AzServiceBusTopic</span></span>

## <span data-ttu-id="11ee1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="11ee1-102">SYNOPSIS</span></span>
<span data-ttu-id="11ee1-103">從指定的 Service Bus 命名空間移除主題。</span><span class="sxs-lookup"><span data-stu-id="11ee1-103">Removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="11ee1-104">語法</span><span class="sxs-lookup"><span data-stu-id="11ee1-104">SYNTAX</span></span>

### <span data-ttu-id="11ee1-105">TopicPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="11ee1-105">TopicPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11ee1-106">TopicInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="11ee1-106">TopicInputObjectSet</span></span>
```
Remove-AzServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11ee1-107">TopicResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="11ee1-107">TopicResourceIdSet</span></span>
```
Remove-AzServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11ee1-108">描述</span><span class="sxs-lookup"><span data-stu-id="11ee1-108">DESCRIPTION</span></span>
<span data-ttu-id="11ee1-109">**Remove-AzServiceBusTopic Cmdlet** 會從指定的 Service Bus 命名空間移除主題。</span><span class="sxs-lookup"><span data-stu-id="11ee1-109">The **Remove-AzServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="11ee1-110">例子</span><span class="sxs-lookup"><span data-stu-id="11ee1-110">EXAMPLES</span></span>

### <span data-ttu-id="11ee1-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="11ee1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="11ee1-112">從命名空間 `SB-Topic_exampl1` 移除主題 `SB-Example1` 。</span><span class="sxs-lookup"><span data-stu-id="11ee1-112">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="11ee1-113">範例 2：InputObject - Using Variable：</span><span class="sxs-lookup"><span data-stu-id="11ee1-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusTopic <parmas>
PS C:\> Remove-AzServiceBusTopic -InputObject $inputobject
```

### <span data-ttu-id="11ee1-114">範例 3：InputObject - 使用管道：</span><span class="sxs-lookup"><span data-stu-id="11ee1-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusTopic <parmas> | Remove-AzServiceBusTopic
```

### <span data-ttu-id="11ee1-115">範例 4：ResourceId Using Variable：</span><span class="sxs-lookup"><span data-stu-id="11ee1-115">Example 4: ResourceId Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusTopic <params>
PS C:\> Remove-AzServiceBusTopic -ResourceId $resourceid.Id
```

### <span data-ttu-id="11ee1-116">範例 5：ResourceId Using String 值</span><span class="sxs-lookup"><span data-stu-id="11ee1-116">Example 5: ResourceId Using String value</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## <span data-ttu-id="11ee1-117">參數</span><span class="sxs-lookup"><span data-stu-id="11ee1-117">PARAMETERS</span></span>

### <span data-ttu-id="11ee1-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11ee1-118">-AsJob</span></span>
<span data-ttu-id="11ee1-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11ee1-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11ee1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11ee1-120">-DefaultProfile</span></span>
<span data-ttu-id="11ee1-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="11ee1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11ee1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11ee1-122">-InputObject</span></span>
<span data-ttu-id="11ee1-123">Service Bus 主題物件</span><span class="sxs-lookup"><span data-stu-id="11ee1-123">Service Bus Topic Object</span></span>

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

### <span data-ttu-id="11ee1-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="11ee1-124">-Name</span></span>
<span data-ttu-id="11ee1-125">主題名稱</span><span class="sxs-lookup"><span data-stu-id="11ee1-125">Topic Name</span></span>

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

### <span data-ttu-id="11ee1-126">-命名空間</span><span class="sxs-lookup"><span data-stu-id="11ee1-126">-Namespace</span></span>
<span data-ttu-id="11ee1-127">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="11ee1-127">Namespace Name</span></span>

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

### <span data-ttu-id="11ee1-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11ee1-128">-PassThru</span></span>
<span data-ttu-id="11ee1-129">如果命令成功，指定此選項會返回 True。</span><span class="sxs-lookup"><span data-stu-id="11ee1-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="11ee1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11ee1-130">-ResourceGroupName</span></span>
<span data-ttu-id="11ee1-131">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="11ee1-131">The name of the resource group</span></span>

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

### <span data-ttu-id="11ee1-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11ee1-132">-ResourceId</span></span>
<span data-ttu-id="11ee1-133">Service Bus 主題資源識別碼</span><span class="sxs-lookup"><span data-stu-id="11ee1-133">Service Bus Topic Resource Id</span></span>

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

### <span data-ttu-id="11ee1-134">-確認</span><span class="sxs-lookup"><span data-stu-id="11ee1-134">-Confirm</span></span>
<span data-ttu-id="11ee1-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="11ee1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11ee1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11ee1-136">-WhatIf</span></span>
<span data-ttu-id="11ee1-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="11ee1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11ee1-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11ee1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11ee1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11ee1-139">CommonParameters</span></span>
<span data-ttu-id="11ee1-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="11ee1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11ee1-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="11ee1-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11ee1-142">輸入</span><span class="sxs-lookup"><span data-stu-id="11ee1-142">INPUTS</span></span>

### <span data-ttu-id="11ee1-143">System.String</span><span class="sxs-lookup"><span data-stu-id="11ee1-143">System.String</span></span>

### <span data-ttu-id="11ee1-144">Microsoft.Azure.Commands.ServiceBus.models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="11ee1-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="11ee1-145">輸出</span><span class="sxs-lookup"><span data-stu-id="11ee1-145">OUTPUTS</span></span>

### <span data-ttu-id="11ee1-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="11ee1-146">System.Boolean</span></span>

## <span data-ttu-id="11ee1-147">筆記</span><span class="sxs-lookup"><span data-stu-id="11ee1-147">NOTES</span></span>

## <span data-ttu-id="11ee1-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="11ee1-148">RELATED LINKS</span></span>
