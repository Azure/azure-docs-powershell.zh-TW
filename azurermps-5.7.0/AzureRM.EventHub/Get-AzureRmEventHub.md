---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
ms.openlocfilehash: e87300af80c38fa0f7989836c992fd1baa53ba6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448673"
---
# <span data-ttu-id="609ca-101">Get-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="609ca-101">Get-AzureRmEventHub</span></span>

## <span data-ttu-id="609ca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="609ca-102">SYNOPSIS</span></span>
<span data-ttu-id="609ca-103">取得單一事件中心的詳細資料，或取得事件中心的清單。</span><span class="sxs-lookup"><span data-stu-id="609ca-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="609ca-104">句法</span><span class="sxs-lookup"><span data-stu-id="609ca-104">SYNTAX</span></span>

```
Get-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="609ca-105">說明</span><span class="sxs-lookup"><span data-stu-id="609ca-105">DESCRIPTION</span></span>
<span data-ttu-id="609ca-106">Get-AzureRmEventHub Cmdlet 會傳回事件中心的詳細資料，或返回目前命名空間中所有事件中心的清單。</span><span class="sxs-lookup"><span data-stu-id="609ca-106">The Get-AzureRmEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="609ca-107">如果提供了事件中樞名稱，則會傳回單一事件中心的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="609ca-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="609ca-108">如果未提供事件中樞名稱，則會傳回指定命名空間中的所有事件中心清單。</span><span class="sxs-lookup"><span data-stu-id="609ca-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="609ca-109">示例</span><span class="sxs-lookup"><span data-stu-id="609ca-109">EXAMPLES</span></span>

### <span data-ttu-id="609ca-110">範例1</span><span class="sxs-lookup"><span data-stu-id="609ca-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="609ca-111">傳回事件中心 MyEventHubName 的詳細資料 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="609ca-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="609ca-112">範例2</span><span class="sxs-lookup"><span data-stu-id="609ca-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="609ca-113">傳回命名空間 MyNamespaceName 中的事件中心清單 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="609ca-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="609ca-114">參數</span><span class="sxs-lookup"><span data-stu-id="609ca-114">PARAMETERS</span></span>

### <span data-ttu-id="609ca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="609ca-115">-DefaultProfile</span></span>
<span data-ttu-id="609ca-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="609ca-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="609ca-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="609ca-117">-Name</span></span>
<span data-ttu-id="609ca-118">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="609ca-118">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="609ca-119">-命名空間</span><span class="sxs-lookup"><span data-stu-id="609ca-119">-Namespace</span></span>
<span data-ttu-id="609ca-120">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="609ca-120">Namespace Name</span></span>

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

### <span data-ttu-id="609ca-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="609ca-121">-ResourceGroupName</span></span>
<span data-ttu-id="609ca-122">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="609ca-122">Resource Group Name</span></span>

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

### <span data-ttu-id="609ca-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="609ca-123">CommonParameters</span></span>
<span data-ttu-id="609ca-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="609ca-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="609ca-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="609ca-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="609ca-126">輸入</span><span class="sxs-lookup"><span data-stu-id="609ca-126">INPUTS</span></span>

### <span data-ttu-id="609ca-127">System.object</span><span class="sxs-lookup"><span data-stu-id="609ca-127">System.String</span></span>


## <span data-ttu-id="609ca-128">輸出</span><span class="sxs-lookup"><span data-stu-id="609ca-128">OUTPUTS</span></span>

### <span data-ttu-id="609ca-129">[System.object]。清單 ' 1 [PSEventHubAttributes，0.5.0.0，，版本 =，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="609ca-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="609ca-130">筆記</span><span class="sxs-lookup"><span data-stu-id="609ca-130">NOTES</span></span>

## <span data-ttu-id="609ca-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="609ca-131">RELATED LINKS</span></span>
