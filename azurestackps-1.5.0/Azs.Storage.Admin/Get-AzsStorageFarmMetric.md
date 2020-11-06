---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 95ea9afa5d3dce953f4e51e84d011886e4ba5688
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442724"
---
# <span data-ttu-id="16e84-101">Get-AzsStorageFarmMetric</span><span class="sxs-lookup"><span data-stu-id="16e84-101">Get-AzsStorageFarmMetric</span></span>

## <span data-ttu-id="16e84-102">摘要</span><span class="sxs-lookup"><span data-stu-id="16e84-102">SYNOPSIS</span></span>
<span data-ttu-id="16e84-103">傳回儲存伺服器陣列度量的清單。</span><span class="sxs-lookup"><span data-stu-id="16e84-103">Returns a list of storage farm metrics.</span></span>

## <span data-ttu-id="16e84-104">句法</span><span class="sxs-lookup"><span data-stu-id="16e84-104">SYNTAX</span></span>

```
Get-AzsStorageFarmMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="16e84-105">說明</span><span class="sxs-lookup"><span data-stu-id="16e84-105">DESCRIPTION</span></span>
<span data-ttu-id="16e84-106">傳回儲存伺服器陣列度量的清單。</span><span class="sxs-lookup"><span data-stu-id="16e84-106">Returns a list of storage farm metrics.</span></span>

## <span data-ttu-id="16e84-107">示例</span><span class="sxs-lookup"><span data-stu-id="16e84-107">EXAMPLES</span></span>

### <span data-ttu-id="16e84-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="16e84-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageFarmMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="16e84-109">取得儲存伺服器陣列度量的清單。</span><span class="sxs-lookup"><span data-stu-id="16e84-109">Get the list of storage farm metrics.</span></span>

## <span data-ttu-id="16e84-110">參數</span><span class="sxs-lookup"><span data-stu-id="16e84-110">PARAMETERS</span></span>

### <span data-ttu-id="16e84-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="16e84-111">-FarmName</span></span>
<span data-ttu-id="16e84-112">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="16e84-112">Farm Id.</span></span>

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

### <span data-ttu-id="16e84-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16e84-113">-ResourceGroupName</span></span>
<span data-ttu-id="16e84-114">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="16e84-114">Resource group name.</span></span>

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

### <span data-ttu-id="16e84-115">-略過</span><span class="sxs-lookup"><span data-stu-id="16e84-115">-Skip</span></span>
<span data-ttu-id="16e84-116">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="16e84-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="16e84-117">-上方</span><span class="sxs-lookup"><span data-stu-id="16e84-117">-Top</span></span>
<span data-ttu-id="16e84-118">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="16e84-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="16e84-119">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="16e84-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="16e84-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e84-120">CommonParameters</span></span>
<span data-ttu-id="16e84-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="16e84-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e84-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="16e84-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e84-123">輸入</span><span class="sxs-lookup"><span data-stu-id="16e84-123">INPUTS</span></span>

## <span data-ttu-id="16e84-124">輸出</span><span class="sxs-lookup"><span data-stu-id="16e84-124">OUTPUTS</span></span>

### <span data-ttu-id="16e84-125">AzureStack （系統管理）。</span><span class="sxs-lookup"><span data-stu-id="16e84-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="16e84-126">筆記</span><span class="sxs-lookup"><span data-stu-id="16e84-126">NOTES</span></span>

## <span data-ttu-id="16e84-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="16e84-127">RELATED LINKS</span></span>

