---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ebe9c71560f18ba9e4d7fb52514a4f5b7007bfb
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/22/2020
ms.locfileid: "93457724"
---
# <span data-ttu-id="f40de-101">Invoke-AzsAzureBridgeProductDownload</span><span class="sxs-lookup"><span data-stu-id="f40de-101">Invoke-AzsAzureBridgeProductDownload</span></span>

## <span data-ttu-id="f40de-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f40de-102">SYNOPSIS</span></span>
<span data-ttu-id="f40de-103">從 azure marketplace 下載產品。</span><span class="sxs-lookup"><span data-stu-id="f40de-103">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="f40de-104">句法</span><span class="sxs-lookup"><span data-stu-id="f40de-104">SYNTAX</span></span>

### <span data-ttu-id="f40de-105">Products_Download (預設) </span><span class="sxs-lookup"><span data-stu-id="f40de-105">Products_Download (Default)</span></span>
```
Invoke-AzsAzureBridgeProductDownload -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f40de-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f40de-106">ResourceId</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f40de-107">說明</span><span class="sxs-lookup"><span data-stu-id="f40de-107">DESCRIPTION</span></span>
<span data-ttu-id="f40de-108">從 azure marketplace 下載產品。</span><span class="sxs-lookup"><span data-stu-id="f40de-108">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="f40de-109">示例</span><span class="sxs-lookup"><span data-stu-id="f40de-109">EXAMPLES</span></span>

### <span data-ttu-id="f40de-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f40de-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ActivationName 'myActivation' -Name 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="f40de-111">從 Azure Marketplace 下載產品</span><span class="sxs-lookup"><span data-stu-id="f40de-111">Download a product from Azure Marketplace</span></span>

## <span data-ttu-id="f40de-112">參數</span><span class="sxs-lookup"><span data-stu-id="f40de-112">PARAMETERS</span></span>

### <span data-ttu-id="f40de-113">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="f40de-113">-ActivationName</span></span>
<span data-ttu-id="f40de-114">啟用的名稱。</span><span class="sxs-lookup"><span data-stu-id="f40de-114">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f40de-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f40de-115">-AsJob</span></span>
<span data-ttu-id="f40de-116">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="f40de-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="f40de-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f40de-117">-Force</span></span>
<span data-ttu-id="f40de-118">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="f40de-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="f40de-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f40de-119">-Name</span></span>
<span data-ttu-id="f40de-120">產品名稱。</span><span class="sxs-lookup"><span data-stu-id="f40de-120">Name of the product.</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f40de-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f40de-121">-ResourceGroupName</span></span>
<span data-ttu-id="f40de-122">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="f40de-122">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f40de-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f40de-123">-ResourceId</span></span>
<span data-ttu-id="f40de-124">Azure 橋接器產品的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f40de-124">Resource identifier for azure bridge product.</span></span>

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

### <span data-ttu-id="f40de-125">-確認</span><span class="sxs-lookup"><span data-stu-id="f40de-125">-Confirm</span></span>
<span data-ttu-id="f40de-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f40de-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f40de-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f40de-127">-WhatIf</span></span>
<span data-ttu-id="f40de-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f40de-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f40de-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f40de-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f40de-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f40de-130">CommonParameters</span></span>
<span data-ttu-id="f40de-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f40de-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f40de-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f40de-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f40de-133">輸入</span><span class="sxs-lookup"><span data-stu-id="f40de-133">INPUTS</span></span>

## <span data-ttu-id="f40de-134">輸出</span><span class="sxs-lookup"><span data-stu-id="f40de-134">OUTPUTS</span></span>

## <span data-ttu-id="f40de-135">筆記</span><span class="sxs-lookup"><span data-stu-id="f40de-135">NOTES</span></span>

## <span data-ttu-id="f40de-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="f40de-136">RELATED LINKS</span></span>

