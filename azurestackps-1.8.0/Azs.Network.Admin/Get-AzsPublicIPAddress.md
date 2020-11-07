---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af3edc04e7db61fa43aa4b192d4bc29d0ec47640
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793676"
---
# <span data-ttu-id="091dd-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="091dd-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="091dd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="091dd-102">SYNOPSIS</span></span>
<span data-ttu-id="091dd-103">公用 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="091dd-103">List of public IP addresses.</span></span>

## <span data-ttu-id="091dd-104">句法</span><span class="sxs-lookup"><span data-stu-id="091dd-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="091dd-105">說明</span><span class="sxs-lookup"><span data-stu-id="091dd-105">DESCRIPTION</span></span>
<span data-ttu-id="091dd-106">公用 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="091dd-106">List of public IP addresses.</span></span>

## <span data-ttu-id="091dd-107">示例</span><span class="sxs-lookup"><span data-stu-id="091dd-107">EXAMPLES</span></span>

### <span data-ttu-id="091dd-108">範例1</span><span class="sxs-lookup"><span data-stu-id="091dd-108">EXAMPLE 1</span></span>
```
Get-AzsPublicIPAddress
```

<span data-ttu-id="091dd-109">取得公用 ip 位址的清單（已指派或未分派）。</span><span class="sxs-lookup"><span data-stu-id="091dd-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="091dd-110">參數</span><span class="sxs-lookup"><span data-stu-id="091dd-110">PARAMETERS</span></span>

### <span data-ttu-id="091dd-111">-篩選</span><span class="sxs-lookup"><span data-stu-id="091dd-111">-Filter</span></span>
<span data-ttu-id="091dd-112">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="091dd-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="091dd-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="091dd-113">-OrderBy</span></span>
<span data-ttu-id="091dd-114">OData orderBy 參數。</span><span class="sxs-lookup"><span data-stu-id="091dd-114">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="091dd-115">-略過</span><span class="sxs-lookup"><span data-stu-id="091dd-115">-Skip</span></span>
<span data-ttu-id="091dd-116">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="091dd-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="091dd-117">-上方</span><span class="sxs-lookup"><span data-stu-id="091dd-117">-Top</span></span>
<span data-ttu-id="091dd-118">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="091dd-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="091dd-119">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="091dd-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="091dd-120">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="091dd-120">-InlineCount</span></span>
<span data-ttu-id="091dd-121">OData 內嵌計數參數。</span><span class="sxs-lookup"><span data-stu-id="091dd-121">OData inline count parameter.</span></span>

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

### <span data-ttu-id="091dd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="091dd-122">CommonParameters</span></span>
<span data-ttu-id="091dd-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="091dd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="091dd-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="091dd-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="091dd-125">輸入</span><span class="sxs-lookup"><span data-stu-id="091dd-125">INPUTS</span></span>

## <span data-ttu-id="091dd-126">輸出</span><span class="sxs-lookup"><span data-stu-id="091dd-126">OUTPUTS</span></span>

### <span data-ttu-id="091dd-127">PublicIpAddress 中的 AzureStack 的管理</span><span class="sxs-lookup"><span data-stu-id="091dd-127">Microsoft.AzureStack.Management.Network.Admin.Models.PublicIpAddress</span></span>

## <span data-ttu-id="091dd-128">筆記</span><span class="sxs-lookup"><span data-stu-id="091dd-128">NOTES</span></span>

## <span data-ttu-id="091dd-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="091dd-129">RELATED LINKS</span></span>
