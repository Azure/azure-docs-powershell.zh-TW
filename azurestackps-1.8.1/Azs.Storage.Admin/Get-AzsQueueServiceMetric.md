---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e2776c768f49dabdea8483ff601f129e80bfc2dc
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793948"
---
# <span data-ttu-id="acc41-101">Get-AzsQueueServiceMetric</span><span class="sxs-lookup"><span data-stu-id="acc41-101">Get-AzsQueueServiceMetric</span></span>

## <span data-ttu-id="acc41-102">摘要</span><span class="sxs-lookup"><span data-stu-id="acc41-102">SYNOPSIS</span></span>
<span data-ttu-id="acc41-103">傳回佇列服務的規格清單。</span><span class="sxs-lookup"><span data-stu-id="acc41-103">Returns a list of metrics for the queue service.</span></span>

## <span data-ttu-id="acc41-104">句法</span><span class="sxs-lookup"><span data-stu-id="acc41-104">SYNTAX</span></span>

```
Get-AzsQueueServiceMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="acc41-105">說明</span><span class="sxs-lookup"><span data-stu-id="acc41-105">DESCRIPTION</span></span>
<span data-ttu-id="acc41-106">傳回佇列服務的規格清單。</span><span class="sxs-lookup"><span data-stu-id="acc41-106">Returns a list of metrics for the queue service.</span></span>

## <span data-ttu-id="acc41-107">示例</span><span class="sxs-lookup"><span data-stu-id="acc41-107">EXAMPLES</span></span>

### <span data-ttu-id="acc41-108">範例1</span><span class="sxs-lookup"><span data-stu-id="acc41-108">EXAMPLE 1</span></span>
```
Get-AzsQueueServiceMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="acc41-109">取得佇列服務的規格清單。</span><span class="sxs-lookup"><span data-stu-id="acc41-109">Get the list of metrics for queue service.</span></span>

## <span data-ttu-id="acc41-110">參數</span><span class="sxs-lookup"><span data-stu-id="acc41-110">PARAMETERS</span></span>

### <span data-ttu-id="acc41-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="acc41-111">-FarmName</span></span>
<span data-ttu-id="acc41-112">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="acc41-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acc41-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acc41-113">-ResourceGroupName</span></span>
<span data-ttu-id="acc41-114">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="acc41-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acc41-115">-略過</span><span class="sxs-lookup"><span data-stu-id="acc41-115">-Skip</span></span>
<span data-ttu-id="acc41-116">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="acc41-116">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acc41-117">-上方</span><span class="sxs-lookup"><span data-stu-id="acc41-117">-Top</span></span>
<span data-ttu-id="acc41-118">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="acc41-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="acc41-119">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="acc41-119">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acc41-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acc41-120">CommonParameters</span></span>
<span data-ttu-id="acc41-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="acc41-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acc41-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="acc41-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acc41-123">輸入</span><span class="sxs-lookup"><span data-stu-id="acc41-123">INPUTS</span></span>

## <span data-ttu-id="acc41-124">輸出</span><span class="sxs-lookup"><span data-stu-id="acc41-124">OUTPUTS</span></span>

### <span data-ttu-id="acc41-125">AzureStack （系統管理）。</span><span class="sxs-lookup"><span data-stu-id="acc41-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="acc41-126">筆記</span><span class="sxs-lookup"><span data-stu-id="acc41-126">NOTES</span></span>

## <span data-ttu-id="acc41-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="acc41-127">RELATED LINKS</span></span>
