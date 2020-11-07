---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c7ca58f806f4d63f2938e3934838a40cbbb113b2
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/26/2020
ms.locfileid: "93968784"
---
# <span data-ttu-id="6b3dd-101">Invoke-AzsAzureBridgeProductDownload</span><span class="sxs-lookup"><span data-stu-id="6b3dd-101">Invoke-AzsAzureBridgeProductDownload</span></span>

## <span data-ttu-id="6b3dd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6b3dd-102">SYNOPSIS</span></span>
<span data-ttu-id="6b3dd-103">從 azure marketplace 下載產品。</span><span class="sxs-lookup"><span data-stu-id="6b3dd-103">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="6b3dd-104">句法</span><span class="sxs-lookup"><span data-stu-id="6b3dd-104">SYNTAX</span></span>

### <span data-ttu-id="6b3dd-105">Products_Download (預設) </span><span class="sxs-lookup"><span data-stu-id="6b3dd-105">Products_Download (Default)</span></span>
```
Invoke-AzsAzureBridgeProductDownload -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b3dd-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b3dd-106">ResourceId</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b3dd-107">說明</span><span class="sxs-lookup"><span data-stu-id="6b3dd-107">DESCRIPTION</span></span>
<span data-ttu-id="6b3dd-108">從 azure marketplace 下載產品。</span><span class="sxs-lookup"><span data-stu-id="6b3dd-108">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="6b3dd-109">示例</span><span class="sxs-lookup"><span data-stu-id="6b3dd-109">EXAMPLES</span></span>

### <span data-ttu-id="6b3dd-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6b3dd-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ActivationName 'myActivation' -Name 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="6b3dd-111">從 Azure Marketplace 下載產品</span><span class="sxs-lookup"><span data-stu-id="6b3dd-111">Download a product from Azure Marketplace</span></span>

## <span data-ttu-id="6b3dd-112">參數</span><span class="sxs-lookup"><span data-stu-id="6b3dd-112">PARAMETERS</span></span>

### <span data-ttu-id="6b3dd-113">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="6b3dd-113">-ActivationName</span></span>
<span data-ttu-id="6b3dd-114">啟用的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b3dd-114">Name of the activation.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b3dd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b3dd-115">-AsJob</span></span>
<span data-ttu-id="6b3dd-116">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="6b3dd-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="6b3dd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6b3dd-117">-Force</span></span>
<span data-ttu-id="6b3dd-118">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="6b3dd-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="6b3dd-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="6b3dd-119">-Name</span></span>
<span data-ttu-id="6b3dd-120">產品名稱。</span><span class="sxs-lookup"><span data-stu-id="6b3dd-120">Name of the product.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b3dd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b3dd-121">-ResourceGroupName</span></span>
<span data-ttu-id="6b3dd-122">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="6b3dd-122">The resource group the resource is located under.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b3dd-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b3dd-123">-ResourceId</span></span>
<span data-ttu-id="6b3dd-124">Azure 橋接器產品的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6b3dd-124">Resource identifier for azure bridge product.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b3dd-125">-確認</span><span class="sxs-lookup"><span data-stu-id="6b3dd-125">-Confirm</span></span>
<span data-ttu-id="6b3dd-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6b3dd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b3dd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b3dd-127">-WhatIf</span></span>
<span data-ttu-id="6b3dd-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6b3dd-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b3dd-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6b3dd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b3dd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b3dd-130">CommonParameters</span></span>
<span data-ttu-id="6b3dd-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6b3dd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b3dd-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6b3dd-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b3dd-133">輸入</span><span class="sxs-lookup"><span data-stu-id="6b3dd-133">INPUTS</span></span>

## <span data-ttu-id="6b3dd-134">輸出</span><span class="sxs-lookup"><span data-stu-id="6b3dd-134">OUTPUTS</span></span>

## <span data-ttu-id="6b3dd-135">筆記</span><span class="sxs-lookup"><span data-stu-id="6b3dd-135">NOTES</span></span>

## <span data-ttu-id="6b3dd-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="6b3dd-136">RELATED LINKS</span></span>

