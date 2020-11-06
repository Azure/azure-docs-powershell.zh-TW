---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: CA67985F-C5D5-4CF4-81A4-C35FD769AF0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmUsage.md
ms.openlocfilehash: 9f02a1c9dfe0c4c41fa1e873201dbeb1d849dd77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453499"
---
# <span data-ttu-id="5e684-101">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="5e684-101">Get-AzureRmUsage</span></span>

## <span data-ttu-id="5e684-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5e684-102">SYNOPSIS</span></span>
<span data-ttu-id="5e684-103">取得資源的使用標準。</span><span class="sxs-lookup"><span data-stu-id="5e684-103">Gets the usage metrics for a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e684-104">句法</span><span class="sxs-lookup"><span data-stu-id="5e684-104">SYNTAX</span></span>

```
Get-AzureRmUsage [-ResourceId] <String> [-ApiVersion <String>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-MetricNames <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e684-105">說明</span><span class="sxs-lookup"><span data-stu-id="5e684-105">DESCRIPTION</span></span>
<span data-ttu-id="5e684-106">**AzureRmUsage** Cmdlet 會取得指定資源的使用衡量標準。</span><span class="sxs-lookup"><span data-stu-id="5e684-106">The **Get-AzureRmUsage** cmdlet gets the usage metrics for a specified resource.</span></span>

## <span data-ttu-id="5e684-107">示例</span><span class="sxs-lookup"><span data-stu-id="5e684-107">EXAMPLES</span></span>

### <span data-ttu-id="5e684-108">範例1：依資源識別碼取得使用方式度量單位</span><span class="sxs-lookup"><span data-stu-id="5e684-108">Example 1: Get usage metrics by resource ID</span></span>
```
PS C:\>Get-AzureRmUsage -ResourceId "/subscriptions/bcdeb07f-1c43-20be-1f3b-4f0febc10f5b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/pattifuller"
```

<span data-ttu-id="5e684-109">這個命令會取得指定網站的使用指標。</span><span class="sxs-lookup"><span data-stu-id="5e684-109">This command gets the usage metrics for the specified website.</span></span>

## <span data-ttu-id="5e684-110">參數</span><span class="sxs-lookup"><span data-stu-id="5e684-110">PARAMETERS</span></span>

### <span data-ttu-id="5e684-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5e684-111">-ApiVersion</span></span>
<span data-ttu-id="5e684-112">指定 API 版本字串（例如，由資源提供者接受的2014-04-01）。</span><span class="sxs-lookup"><span data-stu-id="5e684-112">Specifies an API version string, for example, 2014-04-01, which is accepted by the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e684-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="5e684-113">-EndTime</span></span>
<span data-ttu-id="5e684-114">指定要搜尋的最晚時間與日期。</span><span class="sxs-lookup"><span data-stu-id="5e684-114">Specifies the latest time and date to search.</span></span>

<span data-ttu-id="5e684-115">您可以使用 Get-Date Cmdlet 來取得 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="5e684-115">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e684-116">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="5e684-116">-MetricNames</span></span>
<span data-ttu-id="5e684-117">指定度量單位名稱的陣列。</span><span class="sxs-lookup"><span data-stu-id="5e684-117">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e684-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e684-118">-ResourceId</span></span>
<span data-ttu-id="5e684-119">指定度量的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5e684-119">Specifies the ID of the resource for the metric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e684-120">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5e684-120">-StartTime</span></span>
<span data-ttu-id="5e684-121">指定要搜尋的最早時間與日期。</span><span class="sxs-lookup"><span data-stu-id="5e684-121">Specifies the earliest time and date to search.</span></span>

<span data-ttu-id="5e684-122">您可以使用 Get-Date Cmdlet 來取得 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="5e684-122">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e684-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e684-123">-DefaultProfile</span></span>
<span data-ttu-id="5e684-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5e684-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e684-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e684-125">CommonParameters</span></span>
<span data-ttu-id="5e684-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5e684-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e684-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5e684-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e684-128">輸入</span><span class="sxs-lookup"><span data-stu-id="5e684-128">INPUTS</span></span>

## <span data-ttu-id="5e684-129">輸出</span><span class="sxs-lookup"><span data-stu-id="5e684-129">OUTPUTS</span></span>

### <span data-ttu-id="5e684-130">PSUsageMetric [] 的 OutputClasses []</span><span class="sxs-lookup"><span data-stu-id="5e684-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSUsageMetric[]</span></span>

## <span data-ttu-id="5e684-131">筆記</span><span class="sxs-lookup"><span data-stu-id="5e684-131">NOTES</span></span>

## <span data-ttu-id="5e684-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e684-132">RELATED LINKS</span></span>

[<span data-ttu-id="5e684-133">AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="5e684-133">Get-AzureRmMetric</span></span>](./Get-AzureRmMetric.md)


