---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsoffermetric
schema: 2.0.0
ms.openlocfilehash: 515cf3d9c26c9ca4ed59178e49854e23edfea84c
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966771"
---
# <span data-ttu-id="c22d7-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="c22d7-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="c22d7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c22d7-102">SYNOPSIS</span></span>
<span data-ttu-id="c22d7-103">取得優惠指標。</span><span class="sxs-lookup"><span data-stu-id="c22d7-103">Get the offer metrics.</span></span>

## <span data-ttu-id="c22d7-104">句法</span><span class="sxs-lookup"><span data-stu-id="c22d7-104">SYNTAX</span></span>

```
Get-AzsOfferMetric -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c22d7-105">說明</span><span class="sxs-lookup"><span data-stu-id="c22d7-105">DESCRIPTION</span></span>
<span data-ttu-id="c22d7-106">取得優惠指標。</span><span class="sxs-lookup"><span data-stu-id="c22d7-106">Get the offer metrics.</span></span>

## <span data-ttu-id="c22d7-107">示例</span><span class="sxs-lookup"><span data-stu-id="c22d7-107">EXAMPLES</span></span>

### <span data-ttu-id="c22d7-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c22d7-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsOfferMetric -OfferName "testoffer" -ResourceGroupName "testrg"

EndTime               MetricUnit StartTime            TimeGrain
-------               ---------- ---------            ---------
3/13/2020 12:04:33 AM Count      3/6/2020 12:00:00 AM P1D      
3/13/2020 12:04:33 AM Count      3/6/2020 12:00:00 AM P1D
```

<span data-ttu-id="c22d7-109">取得優惠指標。</span><span class="sxs-lookup"><span data-stu-id="c22d7-109">Get the offer metrics.</span></span>

## <span data-ttu-id="c22d7-110">參數</span><span class="sxs-lookup"><span data-stu-id="c22d7-110">PARAMETERS</span></span>

### <span data-ttu-id="c22d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c22d7-111">-DefaultProfile</span></span>
<span data-ttu-id="c22d7-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c22d7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c22d7-113">-OfferName</span><span class="sxs-lookup"><span data-stu-id="c22d7-113">-OfferName</span></span>
<span data-ttu-id="c22d7-114">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="c22d7-114">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c22d7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c22d7-115">-ResourceGroupName</span></span>
<span data-ttu-id="c22d7-116">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="c22d7-116">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c22d7-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c22d7-117">-SubscriptionId</span></span>
<span data-ttu-id="c22d7-118">可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="c22d7-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c22d7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c22d7-119">CommonParameters</span></span>
<span data-ttu-id="c22d7-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c22d7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c22d7-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c22d7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c22d7-122">輸入</span><span class="sxs-lookup"><span data-stu-id="c22d7-122">INPUTS</span></span>

## <span data-ttu-id="c22d7-123">輸出</span><span class="sxs-lookup"><span data-stu-id="c22d7-123">OUTPUTS</span></span>

### <span data-ttu-id="c22d7-124">IMetricList （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="c22d7-124">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMetricList</span></span>

<span data-ttu-id="c22d7-125">別名</span><span class="sxs-lookup"><span data-stu-id="c22d7-125">ALIASES</span></span>

## <span data-ttu-id="c22d7-126">筆記</span><span class="sxs-lookup"><span data-stu-id="c22d7-126">NOTES</span></span>

## <span data-ttu-id="c22d7-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="c22d7-127">RELATED LINKS</span></span>

