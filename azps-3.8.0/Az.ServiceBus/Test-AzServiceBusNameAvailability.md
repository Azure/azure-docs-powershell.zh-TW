---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
ms.openlocfilehash: adaf7485b0af16821a1f4adec7919422bef07f90
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956824"
---
# <span data-ttu-id="62a78-101">Test-AzServiceBusNameAvailability</span><span class="sxs-lookup"><span data-stu-id="62a78-101">Test-AzServiceBusNameAvailability</span></span>

## <span data-ttu-id="62a78-102">摘要</span><span class="sxs-lookup"><span data-stu-id="62a78-102">SYNOPSIS</span></span>
<span data-ttu-id="62a78-103">檢查指定佇列或主題名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="62a78-103">Checks the Availability of the given Queue or Topic name</span></span>

## <span data-ttu-id="62a78-104">句法</span><span class="sxs-lookup"><span data-stu-id="62a78-104">SYNTAX</span></span>

### <span data-ttu-id="62a78-105">QueueCheckNameAvailabilitySet (預設) </span><span class="sxs-lookup"><span data-stu-id="62a78-105">QueueCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Queue]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62a78-106">TopicCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="62a78-106">TopicCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Topic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62a78-107">說明</span><span class="sxs-lookup"><span data-stu-id="62a78-107">DESCRIPTION</span></span>
<span data-ttu-id="62a78-108">**Test AzServiceBusNameAvailability** Cmdlet 會檢查提供的佇列或主題名稱是否有空</span><span class="sxs-lookup"><span data-stu-id="62a78-108">The **Test-AzServiceBusNameAvailability** Cmdlet Check Availability of the provided Name of Queue or Topic</span></span>

## <span data-ttu-id="62a78-109">示例</span><span class="sxs-lookup"><span data-stu-id="62a78-109">EXAMPLES</span></span>

### <span data-ttu-id="62a78-110">範例1</span><span class="sxs-lookup"><span data-stu-id="62a78-110">Example 1</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameQueue -Queue
True
```

<span data-ttu-id="62a78-111">如果提供的 $nameQueue 名稱是 Availabile，則傳回 True; 如果未提供 $nameQueue 名稱，則傳回 False</span><span class="sxs-lookup"><span data-stu-id="62a78-111">Returns True if the Provided $nameQueue name is Availabile or returns False if Provided $nameQueue name in not available</span></span>

### <span data-ttu-id="62a78-112">範例2</span><span class="sxs-lookup"><span data-stu-id="62a78-112">Example 2</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameTopic -Topic
True
```

<span data-ttu-id="62a78-113">如果提供的 $nameTopic 名稱是 Availabile，則傳回 True; 如果未提供 $nameTopic 名稱，則傳回 False</span><span class="sxs-lookup"><span data-stu-id="62a78-113">Returns True if the Provided $nameTopic name is Availabile or returns False if Provided $nameTopic name in not available</span></span>

## <span data-ttu-id="62a78-114">參數</span><span class="sxs-lookup"><span data-stu-id="62a78-114">PARAMETERS</span></span>

### <span data-ttu-id="62a78-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62a78-115">-DefaultProfile</span></span>
<span data-ttu-id="62a78-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="62a78-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62a78-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="62a78-117">-Name</span></span>
<span data-ttu-id="62a78-118">要檢查名稱可用性的佇列名稱</span><span class="sxs-lookup"><span data-stu-id="62a78-118">Queue Name to check the Name Availability</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62a78-119">-命名空間</span><span class="sxs-lookup"><span data-stu-id="62a78-119">-Namespace</span></span>
<span data-ttu-id="62a78-120">已將命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="62a78-120">Servicebus Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62a78-121">-佇列</span><span class="sxs-lookup"><span data-stu-id="62a78-121">-Queue</span></span>
<span data-ttu-id="62a78-122">檢查佇列名稱的名稱可用性</span><span class="sxs-lookup"><span data-stu-id="62a78-122">To Check Name Availability for Queue Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: QueueCheckNameAvailabilitySet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a78-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62a78-123">-ResourceGroupName</span></span>
<span data-ttu-id="62a78-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="62a78-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62a78-125">-主題</span><span class="sxs-lookup"><span data-stu-id="62a78-125">-Topic</span></span>
<span data-ttu-id="62a78-126">檢查主題名稱的名稱可用性</span><span class="sxs-lookup"><span data-stu-id="62a78-126">To Check Name Availability for Topic Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TopicCheckNameAvailabilitySet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a78-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62a78-127">CommonParameters</span></span>
<span data-ttu-id="62a78-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="62a78-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="62a78-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="62a78-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62a78-130">輸入</span><span class="sxs-lookup"><span data-stu-id="62a78-130">INPUTS</span></span>

### <span data-ttu-id="62a78-131">System.object</span><span class="sxs-lookup"><span data-stu-id="62a78-131">System.String</span></span>

## <span data-ttu-id="62a78-132">輸出</span><span class="sxs-lookup"><span data-stu-id="62a78-132">OUTPUTS</span></span>

### <span data-ttu-id="62a78-133">System.object</span><span class="sxs-lookup"><span data-stu-id="62a78-133">System.Boolean</span></span>

## <span data-ttu-id="62a78-134">筆記</span><span class="sxs-lookup"><span data-stu-id="62a78-134">NOTES</span></span>

## <span data-ttu-id="62a78-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="62a78-135">RELATED LINKS</span></span>
