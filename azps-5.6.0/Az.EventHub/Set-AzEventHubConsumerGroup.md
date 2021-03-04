---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
ms.openlocfilehash: 844b8a08a54409e4eb10cde9f063b65cb5587bae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916569"
---
# <span data-ttu-id="4bf4e-101">Set-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="4bf4e-101">Set-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="4bf4e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4bf4e-102">SYNOPSIS</span></span>
<span data-ttu-id="4bf4e-103">更新指定的事件中樞消費者群組。</span><span class="sxs-lookup"><span data-stu-id="4bf4e-103">Updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="4bf4e-104">語法</span><span class="sxs-lookup"><span data-stu-id="4bf4e-104">SYNTAX</span></span>

```
Set-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4bf4e-105">描述</span><span class="sxs-lookup"><span data-stu-id="4bf4e-105">DESCRIPTION</span></span>
<span data-ttu-id="4bf4e-106">Cmdlet Set-AzEventHubConsumerGroup更新指定的事件中樞消費者群組。</span><span class="sxs-lookup"><span data-stu-id="4bf4e-106">The Set-AzEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="4bf4e-107">例子</span><span class="sxs-lookup"><span data-stu-id="4bf4e-107">EXAMPLES</span></span>

### <span data-ttu-id="4bf4e-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="4bf4e-108">Example 1</span></span>
```
PS C:\> Set-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="4bf4e-109">將消費者群組 \` MyConsumerGroupName 的使用者中繼資料設定 \` 為「測試」。</span><span class="sxs-lookup"><span data-stu-id="4bf4e-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="4bf4e-110">參數</span><span class="sxs-lookup"><span data-stu-id="4bf4e-110">PARAMETERS</span></span>

### <span data-ttu-id="4bf4e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bf4e-111">-DefaultProfile</span></span>
<span data-ttu-id="4bf4e-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4bf4e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bf4e-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="4bf4e-113">-EventHub</span></span>
<span data-ttu-id="4bf4e-114">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="4bf4e-114">EventHub Name</span></span>

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

### <span data-ttu-id="4bf4e-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="4bf4e-115">-Name</span></span>
<span data-ttu-id="4bf4e-116">ConsumerGroup 名稱</span><span class="sxs-lookup"><span data-stu-id="4bf4e-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="4bf4e-117">-命名空間</span><span class="sxs-lookup"><span data-stu-id="4bf4e-117">-Namespace</span></span>
<span data-ttu-id="4bf4e-118">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="4bf4e-118">Namespace Name</span></span>

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

### <span data-ttu-id="4bf4e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bf4e-119">-ResourceGroupName</span></span>
<span data-ttu-id="4bf4e-120">資源組名</span><span class="sxs-lookup"><span data-stu-id="4bf4e-120">Resource Group Name</span></span>

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

### <span data-ttu-id="4bf4e-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="4bf4e-121">-UserMetadata</span></span>
<span data-ttu-id="4bf4e-122">ConsumerGroup 的使用者中繼資料</span><span class="sxs-lookup"><span data-stu-id="4bf4e-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="4bf4e-123">-確認</span><span class="sxs-lookup"><span data-stu-id="4bf4e-123">-Confirm</span></span>
<span data-ttu-id="4bf4e-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4bf4e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bf4e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bf4e-125">-WhatIf</span></span>
<span data-ttu-id="4bf4e-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4bf4e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bf4e-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4bf4e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bf4e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bf4e-128">CommonParameters</span></span>
<span data-ttu-id="4bf4e-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4bf4e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bf4e-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4bf4e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bf4e-131">輸入</span><span class="sxs-lookup"><span data-stu-id="4bf4e-131">INPUTS</span></span>

### <span data-ttu-id="4bf4e-132">System.String</span><span class="sxs-lookup"><span data-stu-id="4bf4e-132">System.String</span></span>

## <span data-ttu-id="4bf4e-133">輸出</span><span class="sxs-lookup"><span data-stu-id="4bf4e-133">OUTPUTS</span></span>

### <span data-ttu-id="4bf4e-134">Microsoft.Azure.Commands.EventHub.models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="4bf4e-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="4bf4e-135">筆記</span><span class="sxs-lookup"><span data-stu-id="4bf4e-135">NOTES</span></span>

## <span data-ttu-id="4bf4e-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="4bf4e-136">RELATED LINKS</span></span>
