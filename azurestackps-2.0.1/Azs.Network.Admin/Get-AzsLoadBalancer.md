---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsloadbalancer
schema: 2.0.0
ms.openlocfilehash: 1450a35252a3bd5e749a8ebdb60fda0e8ad35f88
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966661"
---
# <span data-ttu-id="0476e-101">Get-AzsLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0476e-101">Get-AzsLoadBalancer</span></span>

## <span data-ttu-id="0476e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0476e-102">SYNOPSIS</span></span>
<span data-ttu-id="0476e-103">取得所有負載平衡器的清單。</span><span class="sxs-lookup"><span data-stu-id="0476e-103">Get a list of all load balancers.</span></span>

## <span data-ttu-id="0476e-104">句法</span><span class="sxs-lookup"><span data-stu-id="0476e-104">SYNTAX</span></span>

```
Get-AzsLoadBalancer [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0476e-105">說明</span><span class="sxs-lookup"><span data-stu-id="0476e-105">DESCRIPTION</span></span>
<span data-ttu-id="0476e-106">取得所有負載平衡器的清單。</span><span class="sxs-lookup"><span data-stu-id="0476e-106">Get a list of all load balancers.</span></span>

## <span data-ttu-id="0476e-107">示例</span><span class="sxs-lookup"><span data-stu-id="0476e-107">EXAMPLES</span></span>

### <span data-ttu-id="0476e-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0476e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsLoadBalancer
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsloadbalancer
```



## <span data-ttu-id="0476e-109">參數</span><span class="sxs-lookup"><span data-stu-id="0476e-109">PARAMETERS</span></span>

### <span data-ttu-id="0476e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0476e-110">-DefaultProfile</span></span>
<span data-ttu-id="0476e-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0476e-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0476e-112">-篩選</span><span class="sxs-lookup"><span data-stu-id="0476e-112">-Filter</span></span>
<span data-ttu-id="0476e-113">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="0476e-113">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0476e-114">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="0476e-114">-InlineCount</span></span>
<span data-ttu-id="0476e-115">OData 內嵌計數參數。</span><span class="sxs-lookup"><span data-stu-id="0476e-115">OData inline count parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0476e-116">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="0476e-116">-OrderBy</span></span>
<span data-ttu-id="0476e-117">OData orderBy 參數。</span><span class="sxs-lookup"><span data-stu-id="0476e-117">OData orderBy parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0476e-118">-略過</span><span class="sxs-lookup"><span data-stu-id="0476e-118">-Skip</span></span>
<span data-ttu-id="0476e-119">OData 略過參數。</span><span class="sxs-lookup"><span data-stu-id="0476e-119">OData skip parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0476e-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0476e-120">-SubscriptionId</span></span>
<span data-ttu-id="0476e-121">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="0476e-121">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0476e-122">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="0476e-122">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0476e-123">-上方</span><span class="sxs-lookup"><span data-stu-id="0476e-123">-Top</span></span>
<span data-ttu-id="0476e-124">OData top 參數。</span><span class="sxs-lookup"><span data-stu-id="0476e-124">OData top parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0476e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0476e-125">CommonParameters</span></span>
<span data-ttu-id="0476e-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0476e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0476e-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0476e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0476e-128">輸入</span><span class="sxs-lookup"><span data-stu-id="0476e-128">INPUTS</span></span>

## <span data-ttu-id="0476e-129">輸出</span><span class="sxs-lookup"><span data-stu-id="0476e-129">OUTPUTS</span></span>

### <span data-ttu-id="0476e-130">ILoadBalancer （NetworkAdmin）。 Api20150615。</span><span class="sxs-lookup"><span data-stu-id="0476e-130">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.ILoadBalancer</span></span>



## <span data-ttu-id="0476e-131">筆記</span><span class="sxs-lookup"><span data-stu-id="0476e-131">NOTES</span></span>

## <span data-ttu-id="0476e-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="0476e-132">RELATED LINKS</span></span>

