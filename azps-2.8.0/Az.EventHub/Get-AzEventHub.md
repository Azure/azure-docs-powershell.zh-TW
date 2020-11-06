---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
ms.openlocfilehash: 662c2b5ed487a13c557e85709ed7b850a28acb2e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612441"
---
# <span data-ttu-id="39522-101">Get-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="39522-101">Get-AzEventHub</span></span>

## <span data-ttu-id="39522-102">摘要</span><span class="sxs-lookup"><span data-stu-id="39522-102">SYNOPSIS</span></span>
<span data-ttu-id="39522-103">取得單一事件中心的詳細資料，或取得事件中心的清單。</span><span class="sxs-lookup"><span data-stu-id="39522-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

## <span data-ttu-id="39522-104">句法</span><span class="sxs-lookup"><span data-stu-id="39522-104">SYNTAX</span></span>

```
Get-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39522-105">說明</span><span class="sxs-lookup"><span data-stu-id="39522-105">DESCRIPTION</span></span>
<span data-ttu-id="39522-106">Get-AzEventHub Cmdlet 會傳回事件中心的詳細資料，或返回目前命名空間中所有事件中心的清單。</span><span class="sxs-lookup"><span data-stu-id="39522-106">The Get-AzEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="39522-107">如果提供了事件中樞名稱，則會傳回單一事件中心的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="39522-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="39522-108">如果未提供事件中樞名稱，則會傳回指定命名空間中的所有事件中心清單。</span><span class="sxs-lookup"><span data-stu-id="39522-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="39522-109">示例</span><span class="sxs-lookup"><span data-stu-id="39522-109">EXAMPLES</span></span>

### <span data-ttu-id="39522-110">範例 1-指定 EventHub</span><span class="sxs-lookup"><span data-stu-id="39522-110">Example 1 - specified EventHub</span></span>
```
PS C:\> Get-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="39522-111">傳回事件中心 MyEventHubName 的詳細資料 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="39522-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="39522-112">範例 2-指定命名空間中 EventHub 的清單</span><span class="sxs-lookup"><span data-stu-id="39522-112">Example 2 - List of EventHub in specified Namespace</span></span>
```
PS C:\> Get-AzEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="39522-113">傳回命名空間 MyNamespaceName 中的事件中心清單 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="39522-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="39522-114">參數</span><span class="sxs-lookup"><span data-stu-id="39522-114">PARAMETERS</span></span>

### <span data-ttu-id="39522-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39522-115">-DefaultProfile</span></span>
<span data-ttu-id="39522-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="39522-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39522-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="39522-117">-MaxCount</span></span>
<span data-ttu-id="39522-118">決定要傳回的 EventHubs 數目上限。</span><span class="sxs-lookup"><span data-stu-id="39522-118">Determine the maximum number of EventHubs to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39522-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="39522-119">-Name</span></span>
<span data-ttu-id="39522-120">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="39522-120">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39522-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="39522-121">-Namespace</span></span>
<span data-ttu-id="39522-122">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="39522-122">Namespace Name</span></span>

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

### <span data-ttu-id="39522-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39522-123">-ResourceGroupName</span></span>
<span data-ttu-id="39522-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="39522-124">Resource Group Name</span></span>

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

### <span data-ttu-id="39522-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39522-125">CommonParameters</span></span>
<span data-ttu-id="39522-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="39522-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39522-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="39522-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39522-128">輸入</span><span class="sxs-lookup"><span data-stu-id="39522-128">INPUTS</span></span>

### <span data-ttu-id="39522-129">System.object</span><span class="sxs-lookup"><span data-stu-id="39522-129">System.String</span></span>

## <span data-ttu-id="39522-130">輸出</span><span class="sxs-lookup"><span data-stu-id="39522-130">OUTPUTS</span></span>

### <span data-ttu-id="39522-131">PSEventHubAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="39522-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="39522-132">筆記</span><span class="sxs-lookup"><span data-stu-id="39522-132">NOTES</span></span>

## <span data-ttu-id="39522-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="39522-133">RELATED LINKS</span></span>
