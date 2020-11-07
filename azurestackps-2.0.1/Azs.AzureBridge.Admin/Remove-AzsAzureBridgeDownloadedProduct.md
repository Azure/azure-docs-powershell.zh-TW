---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d75764209b56ed0cc05d80e00581de3f982e435
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/26/2020
ms.locfileid: "93968783"
---
# <span data-ttu-id="05f84-101">Remove-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="05f84-101">Remove-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="05f84-102">摘要</span><span class="sxs-lookup"><span data-stu-id="05f84-102">SYNOPSIS</span></span>
<span data-ttu-id="05f84-103">刪除從 Azure MarketPlace 下載的產品。</span><span class="sxs-lookup"><span data-stu-id="05f84-103">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="05f84-104">句法</span><span class="sxs-lookup"><span data-stu-id="05f84-104">SYNTAX</span></span>

### <span data-ttu-id="05f84-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="05f84-105">Delete (Default)</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-Force] [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05f84-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="05f84-106">ResourceId</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct [-Force] -ResourceId <String> [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05f84-107">說明</span><span class="sxs-lookup"><span data-stu-id="05f84-107">DESCRIPTION</span></span>
<span data-ttu-id="05f84-108">刪除從 Azure MarketPlace 下載的產品。</span><span class="sxs-lookup"><span data-stu-id="05f84-108">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="05f84-109">示例</span><span class="sxs-lookup"><span data-stu-id="05f84-109">EXAMPLES</span></span>

### <span data-ttu-id="05f84-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="05f84-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="05f84-111">刪除從 Azure Marketplace 下載的產品</span><span class="sxs-lookup"><span data-stu-id="05f84-111">Delete a product downloaded from Azure Marketplace</span></span>

## <span data-ttu-id="05f84-112">參數</span><span class="sxs-lookup"><span data-stu-id="05f84-112">PARAMETERS</span></span>

### <span data-ttu-id="05f84-113">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="05f84-113">-ActivationName</span></span>
<span data-ttu-id="05f84-114">啟用的名稱。</span><span class="sxs-lookup"><span data-stu-id="05f84-114">Name of the activation.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05f84-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05f84-115">-AsJob</span></span>
<span data-ttu-id="05f84-116">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="05f84-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="05f84-117">-Force</span><span class="sxs-lookup"><span data-stu-id="05f84-117">-Force</span></span>
<span data-ttu-id="05f84-118">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="05f84-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="05f84-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="05f84-119">-Name</span></span>
<span data-ttu-id="05f84-120">產品名稱。</span><span class="sxs-lookup"><span data-stu-id="05f84-120">Name of the product.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05f84-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05f84-121">-ResourceGroupName</span></span>
<span data-ttu-id="05f84-122">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="05f84-122">The resource group the resource is located under.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05f84-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05f84-123">-ResourceId</span></span>
<span data-ttu-id="05f84-124">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="05f84-124">The resource id.</span></span>

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

### <span data-ttu-id="05f84-125">-確認</span><span class="sxs-lookup"><span data-stu-id="05f84-125">-Confirm</span></span>
<span data-ttu-id="05f84-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="05f84-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05f84-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05f84-127">-WhatIf</span></span>
<span data-ttu-id="05f84-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="05f84-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05f84-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05f84-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05f84-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05f84-130">CommonParameters</span></span>
<span data-ttu-id="05f84-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="05f84-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05f84-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="05f84-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05f84-133">輸入</span><span class="sxs-lookup"><span data-stu-id="05f84-133">INPUTS</span></span>

## <span data-ttu-id="05f84-134">輸出</span><span class="sxs-lookup"><span data-stu-id="05f84-134">OUTPUTS</span></span>

### <span data-ttu-id="05f84-135">AzureStack AzureBridge. DownloadedProductResource （）</span><span class="sxs-lookup"><span data-stu-id="05f84-135">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="05f84-136">筆記</span><span class="sxs-lookup"><span data-stu-id="05f84-136">NOTES</span></span>

## <span data-ttu-id="05f84-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="05f84-137">RELATED LINKS</span></span>

