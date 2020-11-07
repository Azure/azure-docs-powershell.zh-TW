---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8ea8b09e956410184dbc2dd2ed7fa8fc8b89c69b
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793633"
---
# <span data-ttu-id="b6971-101">New-OfferDelegationObject</span><span class="sxs-lookup"><span data-stu-id="b6971-101">New-OfferDelegationObject</span></span>

## <span data-ttu-id="b6971-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b6971-102">SYNOPSIS</span></span>
<span data-ttu-id="b6971-103">提供委派。</span><span class="sxs-lookup"><span data-stu-id="b6971-103">Offer delegation.</span></span>

## <span data-ttu-id="b6971-104">句法</span><span class="sxs-lookup"><span data-stu-id="b6971-104">SYNTAX</span></span>

```
New-OfferDelegationObject [[-Id] <String>] [[-Type] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="b6971-105">說明</span><span class="sxs-lookup"><span data-stu-id="b6971-105">DESCRIPTION</span></span>
<span data-ttu-id="b6971-106">提供委派。</span><span class="sxs-lookup"><span data-stu-id="b6971-106">Offer delegation.</span></span>

## <span data-ttu-id="b6971-107">示例</span><span class="sxs-lookup"><span data-stu-id="b6971-107">EXAMPLES</span></span>

### <span data-ttu-id="b6971-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b6971-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="b6971-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="b6971-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="b6971-110">參數</span><span class="sxs-lookup"><span data-stu-id="b6971-110">PARAMETERS</span></span>

### <span data-ttu-id="b6971-111">-識別碼</span><span class="sxs-lookup"><span data-stu-id="b6971-111">-Id</span></span>
<span data-ttu-id="b6971-112">資源的 URI。</span><span class="sxs-lookup"><span data-stu-id="b6971-112">URI of the resource.</span></span>

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

### <span data-ttu-id="b6971-113">-位置</span><span class="sxs-lookup"><span data-stu-id="b6971-113">-Location</span></span>
<span data-ttu-id="b6971-114">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="b6971-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6971-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="b6971-115">-Name</span></span>
<span data-ttu-id="b6971-116">資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6971-116">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6971-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b6971-117">-SubscriptionId</span></span>
<span data-ttu-id="b6971-118">接收委派優惠之訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b6971-118">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6971-119">-標記</span><span class="sxs-lookup"><span data-stu-id="b6971-119">-Tags</span></span>
<span data-ttu-id="b6971-120">索引鍵/值對清單。</span><span class="sxs-lookup"><span data-stu-id="b6971-120">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6971-121">-類型</span><span class="sxs-lookup"><span data-stu-id="b6971-121">-Type</span></span>
<span data-ttu-id="b6971-122">資源類型。</span><span class="sxs-lookup"><span data-stu-id="b6971-122">Type of resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6971-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6971-123">CommonParameters</span></span>
<span data-ttu-id="b6971-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b6971-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6971-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b6971-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6971-126">輸入</span><span class="sxs-lookup"><span data-stu-id="b6971-126">INPUTS</span></span>

## <span data-ttu-id="b6971-127">輸出</span><span class="sxs-lookup"><span data-stu-id="b6971-127">OUTPUTS</span></span>

## <span data-ttu-id="b6971-128">筆記</span><span class="sxs-lookup"><span data-stu-id="b6971-128">NOTES</span></span>

## <span data-ttu-id="b6971-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6971-129">RELATED LINKS</span></span>

