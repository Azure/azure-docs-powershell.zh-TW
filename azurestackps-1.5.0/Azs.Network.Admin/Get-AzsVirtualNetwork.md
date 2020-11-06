---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 43691cfa3299fc0534ce2d44fd2a2f6ed1043d04
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442760"
---
# <span data-ttu-id="f8e9b-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f8e9b-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="f8e9b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f8e9b-102">SYNOPSIS</span></span>
<span data-ttu-id="f8e9b-103">取得所有虛擬網路的清單。</span><span class="sxs-lookup"><span data-stu-id="f8e9b-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="f8e9b-104">句法</span><span class="sxs-lookup"><span data-stu-id="f8e9b-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="f8e9b-105">說明</span><span class="sxs-lookup"><span data-stu-id="f8e9b-105">DESCRIPTION</span></span>
<span data-ttu-id="f8e9b-106">取得所有虛擬網路的清單。</span><span class="sxs-lookup"><span data-stu-id="f8e9b-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="f8e9b-107">示例</span><span class="sxs-lookup"><span data-stu-id="f8e9b-107">EXAMPLES</span></span>

### <span data-ttu-id="f8e9b-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f8e9b-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVirtualNetwork
```

<span data-ttu-id="f8e9b-109">返回 Azure 堆疊戳記的虛擬網路清單。</span><span class="sxs-lookup"><span data-stu-id="f8e9b-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="f8e9b-110">參數</span><span class="sxs-lookup"><span data-stu-id="f8e9b-110">PARAMETERS</span></span>

### <span data-ttu-id="f8e9b-111">-篩選</span><span class="sxs-lookup"><span data-stu-id="f8e9b-111">-Filter</span></span>
<span data-ttu-id="f8e9b-112">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="f8e9b-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="f8e9b-113">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="f8e9b-113">-InlineCount</span></span>
<span data-ttu-id="f8e9b-114">OData 內嵌計數參數。</span><span class="sxs-lookup"><span data-stu-id="f8e9b-114">OData inline count parameter.</span></span>

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

### <span data-ttu-id="f8e9b-115">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="f8e9b-115">-OrderBy</span></span>
<span data-ttu-id="f8e9b-116">OData orderBy 參數。</span><span class="sxs-lookup"><span data-stu-id="f8e9b-116">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="f8e9b-117">-略過</span><span class="sxs-lookup"><span data-stu-id="f8e9b-117">-Skip</span></span>
<span data-ttu-id="f8e9b-118">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="f8e9b-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="f8e9b-119">-上方</span><span class="sxs-lookup"><span data-stu-id="f8e9b-119">-Top</span></span>
<span data-ttu-id="f8e9b-120">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="f8e9b-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="f8e9b-121">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="f8e9b-121">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="f8e9b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8e9b-122">CommonParameters</span></span>
<span data-ttu-id="f8e9b-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f8e9b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8e9b-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f8e9b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8e9b-125">輸入</span><span class="sxs-lookup"><span data-stu-id="f8e9b-125">INPUTS</span></span>

## <span data-ttu-id="f8e9b-126">輸出</span><span class="sxs-lookup"><span data-stu-id="f8e9b-126">OUTPUTS</span></span>

### <span data-ttu-id="f8e9b-127">VirtualNetwork 中的 AzureStack 的管理</span><span class="sxs-lookup"><span data-stu-id="f8e9b-127">Microsoft.AzureStack.Management.Network.Admin.Models.VirtualNetwork</span></span>

## <span data-ttu-id="f8e9b-128">筆記</span><span class="sxs-lookup"><span data-stu-id="f8e9b-128">NOTES</span></span>

## <span data-ttu-id="f8e9b-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8e9b-129">RELATED LINKS</span></span>

