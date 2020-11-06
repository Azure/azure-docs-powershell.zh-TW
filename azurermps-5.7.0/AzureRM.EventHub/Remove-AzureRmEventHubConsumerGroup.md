---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 5b88ce6edc92cb6483b8d6df95599fcea854f805
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449374"
---
# <span data-ttu-id="54993-101">Remove-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="54993-101">Remove-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="54993-102">摘要</span><span class="sxs-lookup"><span data-stu-id="54993-102">SYNOPSIS</span></span>
<span data-ttu-id="54993-103">刪除指定的事件中樞消費者群組。</span><span class="sxs-lookup"><span data-stu-id="54993-103">Deletes the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54993-104">句法</span><span class="sxs-lookup"><span data-stu-id="54993-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54993-105">說明</span><span class="sxs-lookup"><span data-stu-id="54993-105">DESCRIPTION</span></span>
<span data-ttu-id="54993-106">Remove-AzureRmEventHubConsumerGroup Cmdlet 會從指定的事件中心移除並刪除指定的消費者群組。</span><span class="sxs-lookup"><span data-stu-id="54993-106">The Remove-AzureRmEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="54993-107">示例</span><span class="sxs-lookup"><span data-stu-id="54993-107">EXAMPLES</span></span>

### <span data-ttu-id="54993-108">範例1</span><span class="sxs-lookup"><span data-stu-id="54993-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="54993-109">從事件中心 MyEventHubName 中刪除消費者群組 \` MyConsumerGroupName \` \` \` ，並將其範圍設定為 \` MyNamespaceName \` 命名空間。</span><span class="sxs-lookup"><span data-stu-id="54993-109">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

## <span data-ttu-id="54993-110">參數</span><span class="sxs-lookup"><span data-stu-id="54993-110">PARAMETERS</span></span>

### <span data-ttu-id="54993-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54993-111">-DefaultProfile</span></span>
<span data-ttu-id="54993-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="54993-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54993-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="54993-113">-EventHub</span></span>
<span data-ttu-id="54993-114">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="54993-114">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54993-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="54993-115">-Name</span></span>
<span data-ttu-id="54993-116">ConsumerGroup 名稱</span><span class="sxs-lookup"><span data-stu-id="54993-116">ConsumerGroup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54993-117">-命名空間</span><span class="sxs-lookup"><span data-stu-id="54993-117">-Namespace</span></span>
<span data-ttu-id="54993-118">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="54993-118">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54993-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54993-119">-ResourceGroupName</span></span>
<span data-ttu-id="54993-120">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="54993-120">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54993-121">-確認</span><span class="sxs-lookup"><span data-stu-id="54993-121">-Confirm</span></span>
<span data-ttu-id="54993-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="54993-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54993-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54993-123">-WhatIf</span></span>
<span data-ttu-id="54993-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="54993-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54993-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54993-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54993-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54993-126">CommonParameters</span></span>
<span data-ttu-id="54993-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="54993-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="54993-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="54993-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54993-129">輸入</span><span class="sxs-lookup"><span data-stu-id="54993-129">INPUTS</span></span>

### <span data-ttu-id="54993-130">System.object</span><span class="sxs-lookup"><span data-stu-id="54993-130">System.String</span></span>


## <span data-ttu-id="54993-131">輸出</span><span class="sxs-lookup"><span data-stu-id="54993-131">OUTPUTS</span></span>

### <span data-ttu-id="54993-132">System.object</span><span class="sxs-lookup"><span data-stu-id="54993-132">System.Object</span></span>

## <span data-ttu-id="54993-133">筆記</span><span class="sxs-lookup"><span data-stu-id="54993-133">NOTES</span></span>

## <span data-ttu-id="54993-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="54993-134">RELATED LINKS</span></span>
