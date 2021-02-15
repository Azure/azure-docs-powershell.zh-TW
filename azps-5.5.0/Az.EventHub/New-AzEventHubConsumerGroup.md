---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
ms.openlocfilehash: ef03af9c452496d198aaaa073ee9fd967d851bb4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129355"
---
# <span data-ttu-id="c8a01-101">New-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="c8a01-101">New-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="c8a01-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c8a01-102">SYNOPSIS</span></span>
<span data-ttu-id="c8a01-103">針對指定的事件中心建立新的消費者群組。</span><span class="sxs-lookup"><span data-stu-id="c8a01-103">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="c8a01-104">句法</span><span class="sxs-lookup"><span data-stu-id="c8a01-104">SYNTAX</span></span>

```
New-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c8a01-105">說明</span><span class="sxs-lookup"><span data-stu-id="c8a01-105">DESCRIPTION</span></span>
<span data-ttu-id="c8a01-106">針對指定的事件中心建立新的消費者群組。</span><span class="sxs-lookup"><span data-stu-id="c8a01-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="c8a01-107">示例</span><span class="sxs-lookup"><span data-stu-id="c8a01-107">EXAMPLES</span></span>

### <span data-ttu-id="c8a01-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c8a01-108">Example 1</span></span>
```
PS C:\> New-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="c8a01-109">\` \` 在 \` \` \` \` 包含資源群組 MyResourceGroupName 的命名空間 MyNamespaceName 的 \` 事件中心 MyEventHubName 中 \` 建立消費者群組 MyConsumerGroupName。</span><span class="sxs-lookup"><span data-stu-id="c8a01-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="c8a01-110">參數</span><span class="sxs-lookup"><span data-stu-id="c8a01-110">PARAMETERS</span></span>

### <span data-ttu-id="c8a01-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8a01-111">-DefaultProfile</span></span>
<span data-ttu-id="c8a01-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c8a01-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8a01-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="c8a01-113">-EventHub</span></span>
<span data-ttu-id="c8a01-114">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="c8a01-114">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a01-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="c8a01-115">-Name</span></span>
<span data-ttu-id="c8a01-116">ConsumerGroup 名稱</span><span class="sxs-lookup"><span data-stu-id="c8a01-116">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a01-117">-命名空間</span><span class="sxs-lookup"><span data-stu-id="c8a01-117">-Namespace</span></span>
<span data-ttu-id="c8a01-118">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="c8a01-118">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a01-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8a01-119">-ResourceGroupName</span></span>
<span data-ttu-id="c8a01-120">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="c8a01-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a01-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="c8a01-121">-UserMetadata</span></span>
<span data-ttu-id="c8a01-122">ConsumerGroup 的使用者中繼資料</span><span class="sxs-lookup"><span data-stu-id="c8a01-122">User Metadata for ConsumerGroup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a01-123">-確認</span><span class="sxs-lookup"><span data-stu-id="c8a01-123">-Confirm</span></span>
<span data-ttu-id="c8a01-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c8a01-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8a01-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8a01-125">-WhatIf</span></span>
<span data-ttu-id="c8a01-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c8a01-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8a01-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c8a01-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8a01-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8a01-128">CommonParameters</span></span>
<span data-ttu-id="c8a01-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c8a01-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8a01-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c8a01-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8a01-131">輸入</span><span class="sxs-lookup"><span data-stu-id="c8a01-131">INPUTS</span></span>

### <span data-ttu-id="c8a01-132">System.object</span><span class="sxs-lookup"><span data-stu-id="c8a01-132">System.String</span></span>

## <span data-ttu-id="c8a01-133">輸出</span><span class="sxs-lookup"><span data-stu-id="c8a01-133">OUTPUTS</span></span>

### <span data-ttu-id="c8a01-134">PSConsumerGroupAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="c8a01-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="c8a01-135">筆記</span><span class="sxs-lookup"><span data-stu-id="c8a01-135">NOTES</span></span>

## <span data-ttu-id="c8a01-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8a01-136">RELATED LINKS</span></span>
