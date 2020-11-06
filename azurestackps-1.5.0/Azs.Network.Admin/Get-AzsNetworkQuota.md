---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb5d980efc5f4e4ad7aff13a8f91832589175039
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442764"
---
# <span data-ttu-id="fc679-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="fc679-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="fc679-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fc679-102">SYNOPSIS</span></span>
<span data-ttu-id="fc679-103">列出所有配額。</span><span class="sxs-lookup"><span data-stu-id="fc679-103">List all quotas.</span></span>

## <span data-ttu-id="fc679-104">句法</span><span class="sxs-lookup"><span data-stu-id="fc679-104">SYNTAX</span></span>

### <span data-ttu-id="fc679-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="fc679-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="fc679-106">獲取</span><span class="sxs-lookup"><span data-stu-id="fc679-106">Get</span></span>
```
Get-AzsNetworkQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="fc679-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc679-107">ResourceId</span></span>
```
Get-AzsNetworkQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="fc679-108">說明</span><span class="sxs-lookup"><span data-stu-id="fc679-108">DESCRIPTION</span></span>
<span data-ttu-id="fc679-109">列出所有配額。</span><span class="sxs-lookup"><span data-stu-id="fc679-109">List all quotas.</span></span>
<span data-ttu-id="fc679-110">傳送名稱或篩選限制清單。</span><span class="sxs-lookup"><span data-stu-id="fc679-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="fc679-111">示例</span><span class="sxs-lookup"><span data-stu-id="fc679-111">EXAMPLES</span></span>

### <span data-ttu-id="fc679-112">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fc679-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="fc679-113">列出所有網路配額。</span><span class="sxs-lookup"><span data-stu-id="fc679-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="fc679-114">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="fc679-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="fc679-115">取得指定的網路配額。</span><span class="sxs-lookup"><span data-stu-id="fc679-115">Gets the specified network quota.</span></span>

## <span data-ttu-id="fc679-116">參數</span><span class="sxs-lookup"><span data-stu-id="fc679-116">PARAMETERS</span></span>

### <span data-ttu-id="fc679-117">-篩選</span><span class="sxs-lookup"><span data-stu-id="fc679-117">-Filter</span></span>
<span data-ttu-id="fc679-118">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="fc679-118">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc679-119">-位置</span><span class="sxs-lookup"><span data-stu-id="fc679-119">-Location</span></span>
<span data-ttu-id="fc679-120">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="fc679-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc679-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="fc679-121">-Name</span></span>
<span data-ttu-id="fc679-122">網路配額資源名稱。</span><span class="sxs-lookup"><span data-stu-id="fc679-122">Network quota resource name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc679-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc679-123">-ResourceId</span></span>
<span data-ttu-id="fc679-124">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="fc679-124">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc679-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc679-125">CommonParameters</span></span>
<span data-ttu-id="fc679-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fc679-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc679-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fc679-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc679-128">輸入</span><span class="sxs-lookup"><span data-stu-id="fc679-128">INPUTS</span></span>

## <span data-ttu-id="fc679-129">輸出</span><span class="sxs-lookup"><span data-stu-id="fc679-129">OUTPUTS</span></span>

### <span data-ttu-id="fc679-130">AzureStack. 系統管理員. Quota</span><span class="sxs-lookup"><span data-stu-id="fc679-130">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="fc679-131">筆記</span><span class="sxs-lookup"><span data-stu-id="fc679-131">NOTES</span></span>

## <span data-ttu-id="fc679-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc679-132">RELATED LINKS</span></span>

