---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 987793101e89a7f628f575bf7353994756edaeae
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968432"
---
# <span data-ttu-id="2f0b9-101">Move-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="2f0b9-101">Move-AzsSubscription</span></span>

## <span data-ttu-id="2f0b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2f0b9-102">SYNOPSIS</span></span>
<span data-ttu-id="2f0b9-103">在委派的提供者優惠之間移動訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f0b9-103">Move subscriptions between delegated provider offers.</span></span>

## <span data-ttu-id="2f0b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="2f0b9-104">SYNTAX</span></span>

```
Move-AzsSubscription [[-DestinationDelegatedProviderOffer] <String>] [-ResourceId] <String[]> [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="2f0b9-105">說明</span><span class="sxs-lookup"><span data-stu-id="2f0b9-105">DESCRIPTION</span></span>
<span data-ttu-id="2f0b9-106">在委派的提供者優惠之間移動訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f0b9-106">Move subscriptions between delegated provider offers.</span></span>
<span data-ttu-id="2f0b9-107">這個程式只會執行 rebranding，不會變更訂閱的基礎方案、方案和配額。</span><span class="sxs-lookup"><span data-stu-id="2f0b9-107">This process will only perform a rebranding, the underlying offer, plans, quotas for the subscriptions will not be altered.</span></span>

## <span data-ttu-id="2f0b9-108">示例</span><span class="sxs-lookup"><span data-stu-id="2f0b9-108">EXAMPLES</span></span>

### <span data-ttu-id="2f0b9-109">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2f0b9-109">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Move user subscriptions to a delegated provider offer.
```

<span data-ttu-id="2f0b9-110">Move-AzsSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1"-ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6"，"/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span><span class="sxs-lookup"><span data-stu-id="2f0b9-110">Move-AzsSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1" -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span></span>

### <span data-ttu-id="2f0b9-111">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="2f0b9-111">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Move user subscriptions from a delegated provider to the Default Provider.
```

<span data-ttu-id="2f0b9-112">$resourceIds = Get-AzsUserSubscription-Filter "offerName eq" |其中 {$ _。DelegatedProviderSubscriptionId-eq "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} |選取-ExpandProperty Id Move-AzsSubscription-ResourceId $resourceIds</span><span class="sxs-lookup"><span data-stu-id="2f0b9-112">$resourceIds = Get-AzsUserSubscription -Filter "offerName eq 'o1'" | where {$_.DelegatedProviderSubscriptionId -eq "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | Select -ExpandProperty Id Move-AzsSubscription -ResourceId $resourceIds</span></span>

## <span data-ttu-id="2f0b9-113">參數</span><span class="sxs-lookup"><span data-stu-id="2f0b9-113">PARAMETERS</span></span>

### <span data-ttu-id="2f0b9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f0b9-114">-AsJob</span></span>
<span data-ttu-id="2f0b9-115">指定移動作業是否要作為作業執行。</span><span class="sxs-lookup"><span data-stu-id="2f0b9-115">Specifies whether the move operation is to be executed as a job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0b9-116">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="2f0b9-116">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="2f0b9-117">指定此 Cmdlet 將訂閱移動到哪個完全限定委派提供者提供。</span><span class="sxs-lookup"><span data-stu-id="2f0b9-117">Specifies the fully qualified delegated provider offer into which this cmdlet moves subscriptions.</span></span>
<span data-ttu-id="2f0b9-118">如果要將訂閱移回預設提供者，則為 Null。</span><span class="sxs-lookup"><span data-stu-id="2f0b9-118">NULL if the subscriptions are to be moved back to the Default Provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0b9-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f0b9-119">-ResourceId</span></span>
<span data-ttu-id="2f0b9-120">指定此 Cmdlet 所移動之完整訂閱資源識別碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="2f0b9-120">Specifies an array of fully qualified subscription resource identifiers that this cmdlet moves.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f0b9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f0b9-121">CommonParameters</span></span>
<span data-ttu-id="2f0b9-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2f0b9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f0b9-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2f0b9-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f0b9-124">輸入</span><span class="sxs-lookup"><span data-stu-id="2f0b9-124">INPUTS</span></span>

## <span data-ttu-id="2f0b9-125">輸出</span><span class="sxs-lookup"><span data-stu-id="2f0b9-125">OUTPUTS</span></span>

## <span data-ttu-id="2f0b9-126">筆記</span><span class="sxs-lookup"><span data-stu-id="2f0b9-126">NOTES</span></span>

## <span data-ttu-id="2f0b9-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f0b9-127">RELATED LINKS</span></span>

