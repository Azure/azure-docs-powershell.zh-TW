---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsplanmetric
schema: 2.0.0
ms.openlocfilehash: 9a8ef074cf6e59d30217b55b956a4d5101708bcc
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966647"
---
# <span data-ttu-id="8cdea-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="8cdea-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="8cdea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8cdea-102">SYNOPSIS</span></span>
<span data-ttu-id="8cdea-103">取得指定方案的度量單位。</span><span class="sxs-lookup"><span data-stu-id="8cdea-103">Get the metrics of the specified plan.</span></span>

## <span data-ttu-id="8cdea-104">句法</span><span class="sxs-lookup"><span data-stu-id="8cdea-104">SYNTAX</span></span>

```
Get-AzsPlanMetric -PlanName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8cdea-105">說明</span><span class="sxs-lookup"><span data-stu-id="8cdea-105">DESCRIPTION</span></span>
<span data-ttu-id="8cdea-106">取得指定方案的度量單位。</span><span class="sxs-lookup"><span data-stu-id="8cdea-106">Get the metrics of the specified plan.</span></span>

## <span data-ttu-id="8cdea-107">示例</span><span class="sxs-lookup"><span data-stu-id="8cdea-107">EXAMPLES</span></span>

### <span data-ttu-id="8cdea-108">範例1</span><span class="sxs-lookup"><span data-stu-id="8cdea-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsPlanMetric -PlanName "testplan" -ResourceGroupName "testrg"

EndTime               MetricUnit StartTime            TimeGrain
-------               ---------- ---------            ---------
3/13/2020 12:06:16 AM Count      3/6/2020 12:00:00 AM P1D      
3/13/2020 12:06:16 AM Count      3/6/2020 12:00:00 AM P1D
```

<span data-ttu-id="8cdea-109">取得計畫的度量單位。</span><span class="sxs-lookup"><span data-stu-id="8cdea-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="8cdea-110">參數</span><span class="sxs-lookup"><span data-stu-id="8cdea-110">PARAMETERS</span></span>

### <span data-ttu-id="8cdea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cdea-111">-DefaultProfile</span></span>
<span data-ttu-id="8cdea-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8cdea-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cdea-113">-PlanName</span><span class="sxs-lookup"><span data-stu-id="8cdea-113">-PlanName</span></span>
<span data-ttu-id="8cdea-114">方案名稱。</span><span class="sxs-lookup"><span data-stu-id="8cdea-114">Name of the plan.</span></span>

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

### <span data-ttu-id="8cdea-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cdea-115">-ResourceGroupName</span></span>
<span data-ttu-id="8cdea-116">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="8cdea-116">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="8cdea-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8cdea-117">-SubscriptionId</span></span>
<span data-ttu-id="8cdea-118">可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="8cdea-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8cdea-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cdea-119">CommonParameters</span></span>
<span data-ttu-id="8cdea-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8cdea-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cdea-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8cdea-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cdea-122">輸入</span><span class="sxs-lookup"><span data-stu-id="8cdea-122">INPUTS</span></span>

## <span data-ttu-id="8cdea-123">輸出</span><span class="sxs-lookup"><span data-stu-id="8cdea-123">OUTPUTS</span></span>

### <span data-ttu-id="8cdea-124">IMetricList （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="8cdea-124">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMetricList</span></span>

<span data-ttu-id="8cdea-125">別名</span><span class="sxs-lookup"><span data-stu-id="8cdea-125">ALIASES</span></span>

## <span data-ttu-id="8cdea-126">筆記</span><span class="sxs-lookup"><span data-stu-id="8cdea-126">NOTES</span></span>

## <span data-ttu-id="8cdea-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="8cdea-127">RELATED LINKS</span></span>
