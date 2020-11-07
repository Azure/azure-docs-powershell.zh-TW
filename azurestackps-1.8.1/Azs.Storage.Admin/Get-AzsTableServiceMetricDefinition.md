---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f5d91226a4762c5f1429d8d05b48defd83b4e2df
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93794022"
---
# <span data-ttu-id="b08c3-101">Get-AzsTableServiceMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="b08c3-101">Get-AzsTableServiceMetricDefinition</span></span>

## <span data-ttu-id="b08c3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b08c3-102">SYNOPSIS</span></span>
<span data-ttu-id="b08c3-103">傳回資料表服務的度量定義清單。</span><span class="sxs-lookup"><span data-stu-id="b08c3-103">Returns a list of metric definitions for table service.</span></span>

## <span data-ttu-id="b08c3-104">句法</span><span class="sxs-lookup"><span data-stu-id="b08c3-104">SYNTAX</span></span>

```
Get-AzsTableServiceMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="b08c3-105">說明</span><span class="sxs-lookup"><span data-stu-id="b08c3-105">DESCRIPTION</span></span>
<span data-ttu-id="b08c3-106">傳回資料表服務的度量定義清單。</span><span class="sxs-lookup"><span data-stu-id="b08c3-106">Returns a list of metric definitions for table service.</span></span>

## <span data-ttu-id="b08c3-107">示例</span><span class="sxs-lookup"><span data-stu-id="b08c3-107">EXAMPLES</span></span>

### <span data-ttu-id="b08c3-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b08c3-108">EXAMPLE 1</span></span>
```
Get-AzsTableServiceMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="b08c3-109">取得資料表服務的度量定義清單。</span><span class="sxs-lookup"><span data-stu-id="b08c3-109">Get the list of metric definitions for table service.</span></span>

## <span data-ttu-id="b08c3-110">參數</span><span class="sxs-lookup"><span data-stu-id="b08c3-110">PARAMETERS</span></span>

### <span data-ttu-id="b08c3-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="b08c3-111">-FarmName</span></span>
<span data-ttu-id="b08c3-112">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="b08c3-112">Farm Id.</span></span>

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

### <span data-ttu-id="b08c3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b08c3-113">-ResourceGroupName</span></span>
<span data-ttu-id="b08c3-114">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="b08c3-114">Resource group name.</span></span>

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

### <span data-ttu-id="b08c3-115">-略過</span><span class="sxs-lookup"><span data-stu-id="b08c3-115">-Skip</span></span>
<span data-ttu-id="b08c3-116">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="b08c3-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b08c3-117">-上方</span><span class="sxs-lookup"><span data-stu-id="b08c3-117">-Top</span></span>
<span data-ttu-id="b08c3-118">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="b08c3-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b08c3-119">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="b08c3-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b08c3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b08c3-120">CommonParameters</span></span>
<span data-ttu-id="b08c3-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b08c3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b08c3-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b08c3-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b08c3-123">輸入</span><span class="sxs-lookup"><span data-stu-id="b08c3-123">INPUTS</span></span>

## <span data-ttu-id="b08c3-124">輸出</span><span class="sxs-lookup"><span data-stu-id="b08c3-124">OUTPUTS</span></span>

### <span data-ttu-id="b08c3-125">AzureStack （MetricDefinition）的</span><span class="sxs-lookup"><span data-stu-id="b08c3-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="b08c3-126">筆記</span><span class="sxs-lookup"><span data-stu-id="b08c3-126">NOTES</span></span>

## <span data-ttu-id="b08c3-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="b08c3-127">RELATED LINKS</span></span>
