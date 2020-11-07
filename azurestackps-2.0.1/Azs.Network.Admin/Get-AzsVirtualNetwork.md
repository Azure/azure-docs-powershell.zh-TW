---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsvirtualnetwork
schema: 2.0.0
ms.openlocfilehash: 2f03d0599a7bfaf2b083b4a6c335b1de98b3fa73
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966709"
---
# <span data-ttu-id="c755b-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c755b-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="c755b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c755b-102">SYNOPSIS</span></span>
<span data-ttu-id="c755b-103">取得所有虛擬網路的清單。</span><span class="sxs-lookup"><span data-stu-id="c755b-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="c755b-104">句法</span><span class="sxs-lookup"><span data-stu-id="c755b-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c755b-105">說明</span><span class="sxs-lookup"><span data-stu-id="c755b-105">DESCRIPTION</span></span>
<span data-ttu-id="c755b-106">取得所有虛擬網路的清單。</span><span class="sxs-lookup"><span data-stu-id="c755b-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="c755b-107">示例</span><span class="sxs-lookup"><span data-stu-id="c755b-107">EXAMPLES</span></span>

### <span data-ttu-id="c755b-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c755b-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsVirtualNetwork
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsvirtualnetwork
```

<span data-ttu-id="c755b-109">返回 Azure 堆疊戳記的虛擬網路清單。</span><span class="sxs-lookup"><span data-stu-id="c755b-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="c755b-110">參數</span><span class="sxs-lookup"><span data-stu-id="c755b-110">PARAMETERS</span></span>

### <span data-ttu-id="c755b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c755b-111">-DefaultProfile</span></span>
<span data-ttu-id="c755b-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c755b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c755b-113">-篩選</span><span class="sxs-lookup"><span data-stu-id="c755b-113">-Filter</span></span>
<span data-ttu-id="c755b-114">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="c755b-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="c755b-115">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="c755b-115">-InlineCount</span></span>
<span data-ttu-id="c755b-116">OData 內嵌計數參數。</span><span class="sxs-lookup"><span data-stu-id="c755b-116">OData inline count parameter.</span></span>

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

### <span data-ttu-id="c755b-117">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="c755b-117">-OrderBy</span></span>
<span data-ttu-id="c755b-118">OData orderBy 參數。</span><span class="sxs-lookup"><span data-stu-id="c755b-118">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="c755b-119">-略過</span><span class="sxs-lookup"><span data-stu-id="c755b-119">-Skip</span></span>
<span data-ttu-id="c755b-120">OData 略過參數。</span><span class="sxs-lookup"><span data-stu-id="c755b-120">OData skip parameter.</span></span>

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

### <span data-ttu-id="c755b-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c755b-121">-SubscriptionId</span></span>
<span data-ttu-id="c755b-122">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="c755b-122">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c755b-123">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="c755b-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c755b-124">-上方</span><span class="sxs-lookup"><span data-stu-id="c755b-124">-Top</span></span>
<span data-ttu-id="c755b-125">OData top 參數。</span><span class="sxs-lookup"><span data-stu-id="c755b-125">OData top parameter.</span></span>

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

### <span data-ttu-id="c755b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c755b-126">CommonParameters</span></span>
<span data-ttu-id="c755b-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c755b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c755b-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c755b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c755b-129">輸入</span><span class="sxs-lookup"><span data-stu-id="c755b-129">INPUTS</span></span>

## <span data-ttu-id="c755b-130">輸出</span><span class="sxs-lookup"><span data-stu-id="c755b-130">OUTPUTS</span></span>

### <span data-ttu-id="c755b-131">IVirtualNetwork （NetworkAdmin）。 Api20150615。</span><span class="sxs-lookup"><span data-stu-id="c755b-131">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IVirtualNetwork</span></span>



## <span data-ttu-id="c755b-132">筆記</span><span class="sxs-lookup"><span data-stu-id="c755b-132">NOTES</span></span>

## <span data-ttu-id="c755b-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="c755b-133">RELATED LINKS</span></span>

