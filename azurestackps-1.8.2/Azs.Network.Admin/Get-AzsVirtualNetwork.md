---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af35419f3e0b28be9782e7bbe5d4eaaf1cdf0807
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968409"
---
# <span data-ttu-id="2a326-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2a326-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="2a326-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2a326-102">SYNOPSIS</span></span>
<span data-ttu-id="2a326-103">取得所有虛擬網路的清單。</span><span class="sxs-lookup"><span data-stu-id="2a326-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="2a326-104">句法</span><span class="sxs-lookup"><span data-stu-id="2a326-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="2a326-105">說明</span><span class="sxs-lookup"><span data-stu-id="2a326-105">DESCRIPTION</span></span>
<span data-ttu-id="2a326-106">取得所有虛擬網路的清單。</span><span class="sxs-lookup"><span data-stu-id="2a326-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="2a326-107">示例</span><span class="sxs-lookup"><span data-stu-id="2a326-107">EXAMPLES</span></span>

### <span data-ttu-id="2a326-108">範例1</span><span class="sxs-lookup"><span data-stu-id="2a326-108">EXAMPLE 1</span></span>
```
Get-AzsVirtualNetwork
```

<span data-ttu-id="2a326-109">返回 Azure 堆疊戳記的虛擬網路清單。</span><span class="sxs-lookup"><span data-stu-id="2a326-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="2a326-110">參數</span><span class="sxs-lookup"><span data-stu-id="2a326-110">PARAMETERS</span></span>

### <span data-ttu-id="2a326-111">-篩選</span><span class="sxs-lookup"><span data-stu-id="2a326-111">-Filter</span></span>
<span data-ttu-id="2a326-112">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="2a326-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="2a326-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="2a326-113">-OrderBy</span></span>
<span data-ttu-id="2a326-114">OData orderBy 參數。</span><span class="sxs-lookup"><span data-stu-id="2a326-114">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="2a326-115">-略過</span><span class="sxs-lookup"><span data-stu-id="2a326-115">-Skip</span></span>
<span data-ttu-id="2a326-116">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="2a326-116">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a326-117">-上方</span><span class="sxs-lookup"><span data-stu-id="2a326-117">-Top</span></span>
<span data-ttu-id="2a326-118">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="2a326-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="2a326-119">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="2a326-119">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a326-120">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="2a326-120">-InlineCount</span></span>
<span data-ttu-id="2a326-121">OData 內嵌計數參數。</span><span class="sxs-lookup"><span data-stu-id="2a326-121">OData inline count parameter.</span></span>

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

### <span data-ttu-id="2a326-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a326-122">CommonParameters</span></span>
<span data-ttu-id="2a326-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2a326-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a326-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2a326-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a326-125">輸入</span><span class="sxs-lookup"><span data-stu-id="2a326-125">INPUTS</span></span>

## <span data-ttu-id="2a326-126">輸出</span><span class="sxs-lookup"><span data-stu-id="2a326-126">OUTPUTS</span></span>

### <span data-ttu-id="2a326-127">VirtualNetwork 中的 AzureStack 的管理</span><span class="sxs-lookup"><span data-stu-id="2a326-127">Microsoft.AzureStack.Management.Network.Admin.Models.VirtualNetwork</span></span>

## <span data-ttu-id="2a326-128">筆記</span><span class="sxs-lookup"><span data-stu-id="2a326-128">NOTES</span></span>

## <span data-ttu-id="2a326-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a326-129">RELATED LINKS</span></span>
