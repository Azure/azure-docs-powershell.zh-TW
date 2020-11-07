---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a04836e2d361f4c9686fa5dfe62babfa57ade189
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968531"
---
# <span data-ttu-id="5a266-101">Test-AzsMoveSubscription</span><span class="sxs-lookup"><span data-stu-id="5a266-101">Test-AzsMoveSubscription</span></span>

## <span data-ttu-id="5a266-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5a266-102">SYNOPSIS</span></span>
<span data-ttu-id="5a266-103">確認使用者訂閱可以在委派的提供者提供的服務之間移動。</span><span class="sxs-lookup"><span data-stu-id="5a266-103">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="5a266-104">句法</span><span class="sxs-lookup"><span data-stu-id="5a266-104">SYNTAX</span></span>

```
Test-AzsMoveSubscription [[-DestinationDelegatedProviderOffer] <String>] [-ResourceId] <String[]> [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="5a266-105">說明</span><span class="sxs-lookup"><span data-stu-id="5a266-105">DESCRIPTION</span></span>
<span data-ttu-id="5a266-106">確認使用者訂閱可以在委派的提供者提供的服務之間移動。</span><span class="sxs-lookup"><span data-stu-id="5a266-106">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="5a266-107">示例</span><span class="sxs-lookup"><span data-stu-id="5a266-107">EXAMPLES</span></span>

### <span data-ttu-id="5a266-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5a266-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test that user subscriptions can be moved to a delegated provider offer.
```

<span data-ttu-id="5a266-109">Test-MoveSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1"-ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6"，"/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span><span class="sxs-lookup"><span data-stu-id="5a266-109">Test-MoveSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1" -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span></span>

### <span data-ttu-id="5a266-110">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="5a266-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Test that user subscriptions can be moved from a delegated provider to the Default Provider.
```

<span data-ttu-id="5a266-111">$resourceIds = Get-AzsUserSubscription-Filter "offerName eq" |Select-ExpandProperty Id Test-MoveSubscription-ResoruceId $resourceIds</span><span class="sxs-lookup"><span data-stu-id="5a266-111">$resourceIds = Get-AzsUserSubscription -Filter "offerName eq 'o1'" | Select -ExpandProperty Id Test-MoveSubscription -ResoruceId $resourceIds</span></span>

## <span data-ttu-id="5a266-112">參數</span><span class="sxs-lookup"><span data-stu-id="5a266-112">PARAMETERS</span></span>

### <span data-ttu-id="5a266-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a266-113">-AsJob</span></span>
<span data-ttu-id="5a266-114">指定移動作業是否要作為作業執行。</span><span class="sxs-lookup"><span data-stu-id="5a266-114">Specifies whether the move operation is to be executed as a job.</span></span>

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

### <span data-ttu-id="5a266-115">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="5a266-115">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="5a266-116">指定此 Cmdlet 將訂閱移動到哪個完全限定委派提供者提供。</span><span class="sxs-lookup"><span data-stu-id="5a266-116">Specifies the fully qualified delegated provider offer into which this cmdlet moves subscriptions.</span></span>
<span data-ttu-id="5a266-117">如果要將訂閱移回預設提供者，則為 Null。</span><span class="sxs-lookup"><span data-stu-id="5a266-117">NULL if the subscriptions are to be moved back to the Default Provider.</span></span>

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

### <span data-ttu-id="5a266-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a266-118">-ResourceId</span></span>
<span data-ttu-id="5a266-119">指定此 Cmdlet 所移動之完整訂閱資源識別碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="5a266-119">Specifies an array of fully qualified subscription resource identifiers that this cmdlet moves.</span></span>

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

### <span data-ttu-id="5a266-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a266-120">CommonParameters</span></span>
<span data-ttu-id="5a266-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5a266-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a266-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5a266-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a266-123">輸入</span><span class="sxs-lookup"><span data-stu-id="5a266-123">INPUTS</span></span>

## <span data-ttu-id="5a266-124">輸出</span><span class="sxs-lookup"><span data-stu-id="5a266-124">OUTPUTS</span></span>

## <span data-ttu-id="5a266-125">筆記</span><span class="sxs-lookup"><span data-stu-id="5a266-125">NOTES</span></span>

## <span data-ttu-id="5a266-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a266-126">RELATED LINKS</span></span>

