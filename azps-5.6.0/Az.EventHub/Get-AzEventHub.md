---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
ms.openlocfilehash: d69e30ff993d2e07c7711d36d8e5ec889bc0f7c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916414"
---
# <span data-ttu-id="7d4ff-101">Get-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="7d4ff-101">Get-AzEventHub</span></span>

## <span data-ttu-id="7d4ff-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7d4ff-102">SYNOPSIS</span></span>
<span data-ttu-id="7d4ff-103">獲得單一事件中樞的詳細資訊，或獲得事件中樞清單。</span><span class="sxs-lookup"><span data-stu-id="7d4ff-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

## <span data-ttu-id="7d4ff-104">語法</span><span class="sxs-lookup"><span data-stu-id="7d4ff-104">SYNTAX</span></span>

```
Get-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d4ff-105">描述</span><span class="sxs-lookup"><span data-stu-id="7d4ff-105">DESCRIPTION</span></span>
<span data-ttu-id="7d4ff-106">此Get-AzEventHub Cmdlet 會返回事件中樞詳細資料，或目前命名空間中所有事件中樞的清單。</span><span class="sxs-lookup"><span data-stu-id="7d4ff-106">The Get-AzEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="7d4ff-107">如果提供事件中樞名稱，則會返回單一事件中樞詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7d4ff-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="7d4ff-108">如果未提供事件中樞名稱，會返回指定命名空間中所有事件中樞的清單。</span><span class="sxs-lookup"><span data-stu-id="7d4ff-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="7d4ff-109">例子</span><span class="sxs-lookup"><span data-stu-id="7d4ff-109">EXAMPLES</span></span>

### <span data-ttu-id="7d4ff-110">範例 1：指定的 EventHub</span><span class="sxs-lookup"><span data-stu-id="7d4ff-110">Example 1: specified EventHub</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="7d4ff-111">會返回事件中樞 \` MyEventHubName 的詳細資訊 \` 。</span><span class="sxs-lookup"><span data-stu-id="7d4ff-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="7d4ff-112">範例 2：指定命名空間中的 EventHub 清單</span><span class="sxs-lookup"><span data-stu-id="7d4ff-112">Example 2: List of EventHub in specified Namespace</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="7d4ff-113">會返回命名空間 \` MyNamespaceName 中的事件中樞清單 \` 。</span><span class="sxs-lookup"><span data-stu-id="7d4ff-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="7d4ff-114">參數</span><span class="sxs-lookup"><span data-stu-id="7d4ff-114">PARAMETERS</span></span>

### <span data-ttu-id="7d4ff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d4ff-115">-DefaultProfile</span></span>
<span data-ttu-id="7d4ff-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d4ff-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d4ff-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="7d4ff-117">-MaxCount</span></span>
<span data-ttu-id="7d4ff-118">決定要退回的 EventHub 數量上限。</span><span class="sxs-lookup"><span data-stu-id="7d4ff-118">Determine the maximum number of EventHubs to return.</span></span>

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

### <span data-ttu-id="7d4ff-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="7d4ff-119">-Name</span></span>
<span data-ttu-id="7d4ff-120">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="7d4ff-120">EventHub Name</span></span>

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

### <span data-ttu-id="7d4ff-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="7d4ff-121">-Namespace</span></span>
<span data-ttu-id="7d4ff-122">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="7d4ff-122">Namespace Name</span></span>

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

### <span data-ttu-id="7d4ff-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d4ff-123">-ResourceGroupName</span></span>
<span data-ttu-id="7d4ff-124">資源組名</span><span class="sxs-lookup"><span data-stu-id="7d4ff-124">Resource Group Name</span></span>

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

### <span data-ttu-id="7d4ff-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d4ff-125">CommonParameters</span></span>
<span data-ttu-id="7d4ff-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7d4ff-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d4ff-127">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="7d4ff-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d4ff-128">輸入</span><span class="sxs-lookup"><span data-stu-id="7d4ff-128">INPUTS</span></span>

### <span data-ttu-id="7d4ff-129">System.String</span><span class="sxs-lookup"><span data-stu-id="7d4ff-129">System.String</span></span>

## <span data-ttu-id="7d4ff-130">輸出</span><span class="sxs-lookup"><span data-stu-id="7d4ff-130">OUTPUTS</span></span>

### <span data-ttu-id="7d4ff-131">Microsoft.Azure.Commands.EventHub.models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="7d4ff-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="7d4ff-132">筆記</span><span class="sxs-lookup"><span data-stu-id="7d4ff-132">NOTES</span></span>

## <span data-ttu-id="7d4ff-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d4ff-133">RELATED LINKS</span></span>
