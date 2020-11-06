---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 445d20453b9f3d99e4ff5c72e118b287f0a83898
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454240"
---
# <span data-ttu-id="1128d-101">Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="1128d-101">Get-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="1128d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1128d-102">SYNOPSIS</span></span>
<span data-ttu-id="1128d-103">取得指定事件中樞消費者群組的詳細資料，或取得事件中樞中的消費者群組清單。</span><span class="sxs-lookup"><span data-stu-id="1128d-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1128d-104">句法</span><span class="sxs-lookup"><span data-stu-id="1128d-104">SYNTAX</span></span>

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1128d-105">說明</span><span class="sxs-lookup"><span data-stu-id="1128d-105">DESCRIPTION</span></span>
<span data-ttu-id="1128d-106">Get-AzureRmEventHubConsumerGroup Cmdlet 會取得指定事件中樞消費者群組的詳細資料，或指定事件中樞中的消費者群組清單。</span><span class="sxs-lookup"><span data-stu-id="1128d-106">The Get-AzureRmEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="1128d-107">如果提供消費者群組的名稱，則會傳回單一消費者群組詳細資料的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1128d-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="1128d-108">如果未提供消費者群組的名稱，則會傳回指定事件中樞中的消費者群組清單。</span><span class="sxs-lookup"><span data-stu-id="1128d-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="1128d-109">示例</span><span class="sxs-lookup"><span data-stu-id="1128d-109">EXAMPLES</span></span>

### <span data-ttu-id="1128d-110">範例1</span><span class="sxs-lookup"><span data-stu-id="1128d-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="1128d-111">\` \` 在事件中心 MyEventHubName 中取得消費者群組 MyConsumerGroupName，該活動中心已 \` \` 存在於 \` \` 包含資源群組 MyResourceGroupName 的命名空間 MyNamespaceName 中 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="1128d-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="1128d-112">範例2</span><span class="sxs-lookup"><span data-stu-id="1128d-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="1128d-113">在事件中心 MyEventHubName 中取得消費者群組的清單，該使用者群組 \` \` 存在於 \` \` 包含資源群組 MyResourceGroupName 的命名空間 MyNamespaceName 中 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="1128d-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="1128d-114">參數</span><span class="sxs-lookup"><span data-stu-id="1128d-114">PARAMETERS</span></span>

### <span data-ttu-id="1128d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1128d-115">-DefaultProfile</span></span>
<span data-ttu-id="1128d-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1128d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1128d-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="1128d-117">-EventHub</span></span>
<span data-ttu-id="1128d-118">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="1128d-118">EventHub Name</span></span>

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

### <span data-ttu-id="1128d-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="1128d-119">-Name</span></span>
<span data-ttu-id="1128d-120">ConsumerGroup 名稱</span><span class="sxs-lookup"><span data-stu-id="1128d-120">ConsumerGroup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1128d-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="1128d-121">-Namespace</span></span>
<span data-ttu-id="1128d-122">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="1128d-122">Namespace Name</span></span>

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

### <span data-ttu-id="1128d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1128d-123">-ResourceGroupName</span></span>
<span data-ttu-id="1128d-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="1128d-124">Resource Group Name</span></span>

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

### <span data-ttu-id="1128d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1128d-125">CommonParameters</span></span>
<span data-ttu-id="1128d-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1128d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1128d-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1128d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1128d-128">輸入</span><span class="sxs-lookup"><span data-stu-id="1128d-128">INPUTS</span></span>

### <span data-ttu-id="1128d-129">System.object</span><span class="sxs-lookup"><span data-stu-id="1128d-129">System.String</span></span>


## <span data-ttu-id="1128d-130">輸出</span><span class="sxs-lookup"><span data-stu-id="1128d-130">OUTPUTS</span></span>

### <span data-ttu-id="1128d-131">[System.object]。清單 ' 1 [PSConsumerGroupAttributes，0.5.0.0，，版本 =，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="1128d-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="1128d-132">筆記</span><span class="sxs-lookup"><span data-stu-id="1128d-132">NOTES</span></span>

## <span data-ttu-id="1128d-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="1128d-133">RELATED LINKS</span></span>
