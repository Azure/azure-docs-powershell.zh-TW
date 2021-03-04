---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/test-azservicebusnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
ms.openlocfilehash: b97acb269ee38dc937c5deffb0b3e054b0222c4d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904314"
---
# <span data-ttu-id="ffabb-101">Test-AzServiceBusNameAvailability</span><span class="sxs-lookup"><span data-stu-id="ffabb-101">Test-AzServiceBusNameAvailability</span></span>

## <span data-ttu-id="ffabb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ffabb-102">SYNOPSIS</span></span>
<span data-ttu-id="ffabb-103">檢查指定佇列或主題名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="ffabb-103">Checks the Availability of the given Queue or Topic name</span></span>

## <span data-ttu-id="ffabb-104">語法</span><span class="sxs-lookup"><span data-stu-id="ffabb-104">SYNTAX</span></span>

### <span data-ttu-id="ffabb-105">QueueCheckNameAvailabilitySet (預設) </span><span class="sxs-lookup"><span data-stu-id="ffabb-105">QueueCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Queue]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffabb-106">TopicCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ffabb-106">TopicCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Topic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffabb-107">描述</span><span class="sxs-lookup"><span data-stu-id="ffabb-107">DESCRIPTION</span></span>
<span data-ttu-id="ffabb-108">**Test-AzServiceBusNameAvailability** Cmdlet 檢查提供之佇列或主題名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="ffabb-108">The **Test-AzServiceBusNameAvailability** Cmdlet Check Availability of the provided Name of Queue or Topic</span></span>

## <span data-ttu-id="ffabb-109">例子</span><span class="sxs-lookup"><span data-stu-id="ffabb-109">EXAMPLES</span></span>

### <span data-ttu-id="ffabb-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="ffabb-110">Example 1</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameQueue -Queue
True
```

<span data-ttu-id="ffabb-111">如果提供的$nameQueue名稱為可用值，則$nameQueue為 False</span><span class="sxs-lookup"><span data-stu-id="ffabb-111">Returns True if the Provided $nameQueue name is Availabile or returns False if Provided $nameQueue name in not available</span></span>

### <span data-ttu-id="ffabb-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="ffabb-112">Example 2</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameTopic -Topic
True
```

<span data-ttu-id="ffabb-113">如果提供的$nameTopic名稱為 Availableabile，則$nameTopic為 False;如果提供的功能變數名稱$nameTopic為 False</span><span class="sxs-lookup"><span data-stu-id="ffabb-113">Returns True if the Provided $nameTopic name is Availabile or returns False if Provided $nameTopic name in not available</span></span>

## <span data-ttu-id="ffabb-114">參數</span><span class="sxs-lookup"><span data-stu-id="ffabb-114">PARAMETERS</span></span>

### <span data-ttu-id="ffabb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffabb-115">-DefaultProfile</span></span>
<span data-ttu-id="ffabb-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ffabb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffabb-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="ffabb-117">-Name</span></span>
<span data-ttu-id="ffabb-118">佇列名稱以檢查名稱可用性</span><span class="sxs-lookup"><span data-stu-id="ffabb-118">Queue Name to check the Name Availability</span></span>

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

### <span data-ttu-id="ffabb-119">-命名空間</span><span class="sxs-lookup"><span data-stu-id="ffabb-119">-Namespace</span></span>
<span data-ttu-id="ffabb-120">Servicebus 命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="ffabb-120">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="ffabb-121">-佇列</span><span class="sxs-lookup"><span data-stu-id="ffabb-121">-Queue</span></span>
<span data-ttu-id="ffabb-122">檢查佇列名稱的名稱可用性</span><span class="sxs-lookup"><span data-stu-id="ffabb-122">To Check Name Availability for Queue Name</span></span>

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

### <span data-ttu-id="ffabb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffabb-123">-ResourceGroupName</span></span>
<span data-ttu-id="ffabb-124">資源組名</span><span class="sxs-lookup"><span data-stu-id="ffabb-124">Resource Group Name</span></span>

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

### <span data-ttu-id="ffabb-125">-主題</span><span class="sxs-lookup"><span data-stu-id="ffabb-125">-Topic</span></span>
<span data-ttu-id="ffabb-126">檢查主題名稱的名稱可用性</span><span class="sxs-lookup"><span data-stu-id="ffabb-126">To Check Name Availability for Topic Name</span></span>

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

### <span data-ttu-id="ffabb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffabb-127">CommonParameters</span></span>
<span data-ttu-id="ffabb-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ffabb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ffabb-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ffabb-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffabb-130">輸入</span><span class="sxs-lookup"><span data-stu-id="ffabb-130">INPUTS</span></span>

### <span data-ttu-id="ffabb-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ffabb-131">System.String</span></span>

## <span data-ttu-id="ffabb-132">輸出</span><span class="sxs-lookup"><span data-stu-id="ffabb-132">OUTPUTS</span></span>

### <span data-ttu-id="ffabb-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ffabb-133">System.Boolean</span></span>

## <span data-ttu-id="ffabb-134">筆記</span><span class="sxs-lookup"><span data-stu-id="ffabb-134">NOTES</span></span>

## <span data-ttu-id="ffabb-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="ffabb-135">RELATED LINKS</span></span>
