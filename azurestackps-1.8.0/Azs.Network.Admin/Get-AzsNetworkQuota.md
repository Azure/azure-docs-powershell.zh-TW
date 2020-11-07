---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3def97a3e02e77efd6ec21768b30c855f1ceb34e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793677"
---
# <span data-ttu-id="c9042-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="c9042-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="c9042-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c9042-102">SYNOPSIS</span></span>
<span data-ttu-id="c9042-103">列出所有配額。</span><span class="sxs-lookup"><span data-stu-id="c9042-103">List all quotas.</span></span>

## <span data-ttu-id="c9042-104">句法</span><span class="sxs-lookup"><span data-stu-id="c9042-104">SYNTAX</span></span>

### <span data-ttu-id="c9042-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="c9042-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="c9042-106">獲取</span><span class="sxs-lookup"><span data-stu-id="c9042-106">Get</span></span>
```
Get-AzsNetworkQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="c9042-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9042-107">ResourceId</span></span>
```
Get-AzsNetworkQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c9042-108">說明</span><span class="sxs-lookup"><span data-stu-id="c9042-108">DESCRIPTION</span></span>
<span data-ttu-id="c9042-109">列出所有配額。</span><span class="sxs-lookup"><span data-stu-id="c9042-109">List all quotas.</span></span>
<span data-ttu-id="c9042-110">傳送名稱或篩選限制清單。</span><span class="sxs-lookup"><span data-stu-id="c9042-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="c9042-111">示例</span><span class="sxs-lookup"><span data-stu-id="c9042-111">EXAMPLES</span></span>

### <span data-ttu-id="c9042-112">範例1</span><span class="sxs-lookup"><span data-stu-id="c9042-112">EXAMPLE 1</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="c9042-113">列出所有網路配額。</span><span class="sxs-lookup"><span data-stu-id="c9042-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="c9042-114">範例2</span><span class="sxs-lookup"><span data-stu-id="c9042-114">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="c9042-115">取得指定的網路配額。</span><span class="sxs-lookup"><span data-stu-id="c9042-115">Gets the specified network quota.</span></span>

## <span data-ttu-id="c9042-116">參數</span><span class="sxs-lookup"><span data-stu-id="c9042-116">PARAMETERS</span></span>

### <span data-ttu-id="c9042-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="c9042-117">-Name</span></span>
<span data-ttu-id="c9042-118">網路配額資源名稱。</span><span class="sxs-lookup"><span data-stu-id="c9042-118">Network quota resource name.</span></span>

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

### <span data-ttu-id="c9042-119">-位置</span><span class="sxs-lookup"><span data-stu-id="c9042-119">-Location</span></span>
<span data-ttu-id="c9042-120">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="c9042-120">Location of the resource.</span></span>

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

### <span data-ttu-id="c9042-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9042-121">-ResourceId</span></span>
<span data-ttu-id="c9042-122">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="c9042-122">The resource id.</span></span>

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

### <span data-ttu-id="c9042-123">-篩選</span><span class="sxs-lookup"><span data-stu-id="c9042-123">-Filter</span></span>
<span data-ttu-id="c9042-124">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="c9042-124">OData filter parameter.</span></span>

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

### <span data-ttu-id="c9042-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9042-125">CommonParameters</span></span>
<span data-ttu-id="c9042-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c9042-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9042-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c9042-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9042-128">輸入</span><span class="sxs-lookup"><span data-stu-id="c9042-128">INPUTS</span></span>

## <span data-ttu-id="c9042-129">輸出</span><span class="sxs-lookup"><span data-stu-id="c9042-129">OUTPUTS</span></span>

### <span data-ttu-id="c9042-130">AzureStack. 系統管理員. Quota</span><span class="sxs-lookup"><span data-stu-id="c9042-130">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="c9042-131">筆記</span><span class="sxs-lookup"><span data-stu-id="c9042-131">NOTES</span></span>

## <span data-ttu-id="c9042-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="c9042-132">RELATED LINKS</span></span>
