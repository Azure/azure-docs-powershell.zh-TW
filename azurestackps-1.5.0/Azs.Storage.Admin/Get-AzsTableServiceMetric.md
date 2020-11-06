---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 007f5116c17e9bf2c1df742e0f11c9a86844134b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443592"
---
# <span data-ttu-id="7f063-101">Get-AzsTableServiceMetric</span><span class="sxs-lookup"><span data-stu-id="7f063-101">Get-AzsTableServiceMetric</span></span>

## <span data-ttu-id="7f063-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7f063-102">SYNOPSIS</span></span>
<span data-ttu-id="7f063-103">傳回資料表服務的規格清單。</span><span class="sxs-lookup"><span data-stu-id="7f063-103">Returns a list of metrics for table service.</span></span>

## <span data-ttu-id="7f063-104">句法</span><span class="sxs-lookup"><span data-stu-id="7f063-104">SYNTAX</span></span>

```
Get-AzsTableServiceMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f063-105">說明</span><span class="sxs-lookup"><span data-stu-id="7f063-105">DESCRIPTION</span></span>
<span data-ttu-id="7f063-106">傳回資料表服務的規格清單。</span><span class="sxs-lookup"><span data-stu-id="7f063-106">Returns a list of metrics for table service.</span></span>

## <span data-ttu-id="7f063-107">示例</span><span class="sxs-lookup"><span data-stu-id="7f063-107">EXAMPLES</span></span>

### <span data-ttu-id="7f063-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7f063-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsTableServiceMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="7f063-109">取得資料表服務的規格清單。</span><span class="sxs-lookup"><span data-stu-id="7f063-109">Get the list of metrics for table service.</span></span>

## <span data-ttu-id="7f063-110">參數</span><span class="sxs-lookup"><span data-stu-id="7f063-110">PARAMETERS</span></span>

### <span data-ttu-id="7f063-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="7f063-111">-FarmName</span></span>
<span data-ttu-id="7f063-112">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="7f063-112">Farm Id.</span></span>

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

### <span data-ttu-id="7f063-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f063-113">-ResourceGroupName</span></span>
<span data-ttu-id="7f063-114">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="7f063-114">Resource group name.</span></span>

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

### <span data-ttu-id="7f063-115">-略過</span><span class="sxs-lookup"><span data-stu-id="7f063-115">-Skip</span></span>
<span data-ttu-id="7f063-116">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="7f063-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="7f063-117">-上方</span><span class="sxs-lookup"><span data-stu-id="7f063-117">-Top</span></span>
<span data-ttu-id="7f063-118">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="7f063-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="7f063-119">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="7f063-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="7f063-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f063-120">CommonParameters</span></span>
<span data-ttu-id="7f063-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7f063-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f063-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7f063-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f063-123">輸入</span><span class="sxs-lookup"><span data-stu-id="7f063-123">INPUTS</span></span>

## <span data-ttu-id="7f063-124">輸出</span><span class="sxs-lookup"><span data-stu-id="7f063-124">OUTPUTS</span></span>

### <span data-ttu-id="7f063-125">AzureStack （系統管理）。</span><span class="sxs-lookup"><span data-stu-id="7f063-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="7f063-126">筆記</span><span class="sxs-lookup"><span data-stu-id="7f063-126">NOTES</span></span>

## <span data-ttu-id="7f063-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f063-127">RELATED LINKS</span></span>
