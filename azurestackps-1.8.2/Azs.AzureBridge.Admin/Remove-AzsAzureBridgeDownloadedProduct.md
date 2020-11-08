---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1cc5311b1c26d4ae0cb9c1a7ce6ad58a818b53c6
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/22/2020
ms.locfileid: "94136577"
---
# <span data-ttu-id="46c6d-101">Remove-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="46c6d-101">Remove-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="46c6d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="46c6d-102">SYNOPSIS</span></span>
<span data-ttu-id="46c6d-103">刪除從 Azure MarketPlace 下載的產品。</span><span class="sxs-lookup"><span data-stu-id="46c6d-103">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="46c6d-104">句法</span><span class="sxs-lookup"><span data-stu-id="46c6d-104">SYNTAX</span></span>

### <span data-ttu-id="46c6d-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="46c6d-105">Delete (Default)</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-Force] [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46c6d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="46c6d-106">ResourceId</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct [-Force] -ResourceId <String> [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46c6d-107">說明</span><span class="sxs-lookup"><span data-stu-id="46c6d-107">DESCRIPTION</span></span>
<span data-ttu-id="46c6d-108">刪除從 Azure MarketPlace 下載的產品。</span><span class="sxs-lookup"><span data-stu-id="46c6d-108">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="46c6d-109">示例</span><span class="sxs-lookup"><span data-stu-id="46c6d-109">EXAMPLES</span></span>

### <span data-ttu-id="46c6d-110">範例1</span><span class="sxs-lookup"><span data-stu-id="46c6d-110">EXAMPLE 1</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="46c6d-111">刪除從 Azure Marketplace 下載的產品</span><span class="sxs-lookup"><span data-stu-id="46c6d-111">Delete a product downloaded from Azure Marketplace</span></span>

## <span data-ttu-id="46c6d-112">參數</span><span class="sxs-lookup"><span data-stu-id="46c6d-112">PARAMETERS</span></span>

### <span data-ttu-id="46c6d-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="46c6d-113">-Name</span></span>
<span data-ttu-id="46c6d-114">產品名稱。</span><span class="sxs-lookup"><span data-stu-id="46c6d-114">Name of the product.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46c6d-115">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="46c6d-115">-ActivationName</span></span>
<span data-ttu-id="46c6d-116">啟用的名稱。</span><span class="sxs-lookup"><span data-stu-id="46c6d-116">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46c6d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46c6d-117">-ResourceGroupName</span></span>
<span data-ttu-id="46c6d-118">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="46c6d-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46c6d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="46c6d-119">-Force</span></span>
<span data-ttu-id="46c6d-120">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="46c6d-120">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46c6d-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46c6d-121">-ResourceId</span></span>
<span data-ttu-id="46c6d-122">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="46c6d-122">The resource id.</span></span>

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

### <span data-ttu-id="46c6d-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46c6d-123">-AsJob</span></span>
<span data-ttu-id="46c6d-124">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="46c6d-124">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46c6d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46c6d-125">-WhatIf</span></span>
<span data-ttu-id="46c6d-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="46c6d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46c6d-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46c6d-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46c6d-128">-確認</span><span class="sxs-lookup"><span data-stu-id="46c6d-128">-Confirm</span></span>
<span data-ttu-id="46c6d-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="46c6d-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46c6d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46c6d-130">CommonParameters</span></span>
<span data-ttu-id="46c6d-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="46c6d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46c6d-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="46c6d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46c6d-133">輸入</span><span class="sxs-lookup"><span data-stu-id="46c6d-133">INPUTS</span></span>

## <span data-ttu-id="46c6d-134">輸出</span><span class="sxs-lookup"><span data-stu-id="46c6d-134">OUTPUTS</span></span>

### <span data-ttu-id="46c6d-135">AzureStack AzureBridge. DownloadedProductResource （）</span><span class="sxs-lookup"><span data-stu-id="46c6d-135">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="46c6d-136">筆記</span><span class="sxs-lookup"><span data-stu-id="46c6d-136">NOTES</span></span>

## <span data-ttu-id="46c6d-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="46c6d-137">RELATED LINKS</span></span>
