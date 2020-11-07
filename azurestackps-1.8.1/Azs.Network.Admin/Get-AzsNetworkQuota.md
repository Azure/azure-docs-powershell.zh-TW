---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3def97a3e02e77efd6ec21768b30c855f1ceb34e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793967"
---
# <span data-ttu-id="0860c-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="0860c-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="0860c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0860c-102">SYNOPSIS</span></span>
<span data-ttu-id="0860c-103">列出所有配額。</span><span class="sxs-lookup"><span data-stu-id="0860c-103">List all quotas.</span></span>

## <span data-ttu-id="0860c-104">句法</span><span class="sxs-lookup"><span data-stu-id="0860c-104">SYNTAX</span></span>

### <span data-ttu-id="0860c-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="0860c-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="0860c-106">獲取</span><span class="sxs-lookup"><span data-stu-id="0860c-106">Get</span></span>
```
Get-AzsNetworkQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="0860c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0860c-107">ResourceId</span></span>
```
Get-AzsNetworkQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="0860c-108">說明</span><span class="sxs-lookup"><span data-stu-id="0860c-108">DESCRIPTION</span></span>
<span data-ttu-id="0860c-109">列出所有配額。</span><span class="sxs-lookup"><span data-stu-id="0860c-109">List all quotas.</span></span>
<span data-ttu-id="0860c-110">傳送名稱或篩選限制清單。</span><span class="sxs-lookup"><span data-stu-id="0860c-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="0860c-111">示例</span><span class="sxs-lookup"><span data-stu-id="0860c-111">EXAMPLES</span></span>

### <span data-ttu-id="0860c-112">範例1</span><span class="sxs-lookup"><span data-stu-id="0860c-112">EXAMPLE 1</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="0860c-113">列出所有網路配額。</span><span class="sxs-lookup"><span data-stu-id="0860c-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="0860c-114">範例2</span><span class="sxs-lookup"><span data-stu-id="0860c-114">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="0860c-115">取得指定的網路配額。</span><span class="sxs-lookup"><span data-stu-id="0860c-115">Gets the specified network quota.</span></span>

## <span data-ttu-id="0860c-116">參數</span><span class="sxs-lookup"><span data-stu-id="0860c-116">PARAMETERS</span></span>

### <span data-ttu-id="0860c-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="0860c-117">-Name</span></span>
<span data-ttu-id="0860c-118">網路配額資源名稱。</span><span class="sxs-lookup"><span data-stu-id="0860c-118">Network quota resource name.</span></span>

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

### <span data-ttu-id="0860c-119">-位置</span><span class="sxs-lookup"><span data-stu-id="0860c-119">-Location</span></span>
<span data-ttu-id="0860c-120">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="0860c-120">Location of the resource.</span></span>

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

### <span data-ttu-id="0860c-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0860c-121">-ResourceId</span></span>
<span data-ttu-id="0860c-122">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="0860c-122">The resource id.</span></span>

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

### <span data-ttu-id="0860c-123">-篩選</span><span class="sxs-lookup"><span data-stu-id="0860c-123">-Filter</span></span>
<span data-ttu-id="0860c-124">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="0860c-124">OData filter parameter.</span></span>

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

### <span data-ttu-id="0860c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0860c-125">CommonParameters</span></span>
<span data-ttu-id="0860c-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0860c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0860c-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0860c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0860c-128">輸入</span><span class="sxs-lookup"><span data-stu-id="0860c-128">INPUTS</span></span>

## <span data-ttu-id="0860c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="0860c-129">OUTPUTS</span></span>

### <span data-ttu-id="0860c-130">AzureStack. 系統管理員. Quota</span><span class="sxs-lookup"><span data-stu-id="0860c-130">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="0860c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="0860c-131">NOTES</span></span>

## <span data-ttu-id="0860c-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="0860c-132">RELATED LINKS</span></span>
