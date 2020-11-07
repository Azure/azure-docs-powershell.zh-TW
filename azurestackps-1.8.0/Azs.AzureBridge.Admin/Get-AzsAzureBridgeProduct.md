---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c875b28f6518a836296fe1f5f19910d549b880c7
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/22/2020
ms.locfileid: "93802721"
---
# <span data-ttu-id="ff4bd-101">Get-AzsAzureBridgeProduct</span><span class="sxs-lookup"><span data-stu-id="ff4bd-101">Get-AzsAzureBridgeProduct</span></span>

## <span data-ttu-id="ff4bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ff4bd-102">SYNOPSIS</span></span>
<span data-ttu-id="ff4bd-103">傳回可從 Azure Marketplace 下載的產品清單。</span><span class="sxs-lookup"><span data-stu-id="ff4bd-103">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="ff4bd-104">句法</span><span class="sxs-lookup"><span data-stu-id="ff4bd-104">SYNTAX</span></span>

### <span data-ttu-id="ff4bd-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="ff4bd-105">List (Default)</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="ff4bd-106">獲取</span><span class="sxs-lookup"><span data-stu-id="ff4bd-106">Get</span></span>
```
Get-AzsAzureBridgeProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="ff4bd-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff4bd-107">ResourceId</span></span>
```
Get-AzsAzureBridgeProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ff4bd-108">說明</span><span class="sxs-lookup"><span data-stu-id="ff4bd-108">DESCRIPTION</span></span>
<span data-ttu-id="ff4bd-109">傳回可從 Azure Marketplace 下載的產品清單。</span><span class="sxs-lookup"><span data-stu-id="ff4bd-109">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="ff4bd-110">示例</span><span class="sxs-lookup"><span data-stu-id="ff4bd-110">EXAMPLES</span></span>

### <span data-ttu-id="ff4bd-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ff4bd-111">EXAMPLE 1</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="ff4bd-112">取得可從 Azure Marketplace 下載的產品清單。</span><span class="sxs-lookup"><span data-stu-id="ff4bd-112">Get a list of Products available for download from Azure Marketplace.</span></span>

### <span data-ttu-id="ff4bd-113">範例2</span><span class="sxs-lookup"><span data-stu-id="ff4bd-113">EXAMPLE 2</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG' -Name 'microsoft.docker-arm.1.1.0'
```

<span data-ttu-id="ff4bd-114">取得從 Azure Marketplace 透過名稱下載的產品資訊。</span><span class="sxs-lookup"><span data-stu-id="ff4bd-114">Get a product info available for download from Azure Marketplace by Name.</span></span>

## <span data-ttu-id="ff4bd-115">參數</span><span class="sxs-lookup"><span data-stu-id="ff4bd-115">PARAMETERS</span></span>

### <span data-ttu-id="ff4bd-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="ff4bd-116">-Name</span></span>
<span data-ttu-id="ff4bd-117">產品名稱。</span><span class="sxs-lookup"><span data-stu-id="ff4bd-117">Name of the product.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff4bd-118">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="ff4bd-118">-ActivationName</span></span>
<span data-ttu-id="ff4bd-119">啟用的名稱。</span><span class="sxs-lookup"><span data-stu-id="ff4bd-119">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff4bd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff4bd-120">-ResourceGroupName</span></span>
<span data-ttu-id="ff4bd-121">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="ff4bd-121">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff4bd-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff4bd-122">-ResourceId</span></span>
<span data-ttu-id="ff4bd-123">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="ff4bd-123">The resource id.</span></span>

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

### <span data-ttu-id="ff4bd-124">-略過</span><span class="sxs-lookup"><span data-stu-id="ff4bd-124">-Skip</span></span>
<span data-ttu-id="ff4bd-125">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="ff4bd-125">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff4bd-126">-上方</span><span class="sxs-lookup"><span data-stu-id="ff4bd-126">-Top</span></span>
<span data-ttu-id="ff4bd-127">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="ff4bd-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ff4bd-128">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="ff4bd-128">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff4bd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff4bd-129">CommonParameters</span></span>
<span data-ttu-id="ff4bd-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ff4bd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff4bd-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ff4bd-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff4bd-132">輸入</span><span class="sxs-lookup"><span data-stu-id="ff4bd-132">INPUTS</span></span>

## <span data-ttu-id="ff4bd-133">輸出</span><span class="sxs-lookup"><span data-stu-id="ff4bd-133">OUTPUTS</span></span>

### <span data-ttu-id="ff4bd-134">AzureStack AzureBridge. ProductResource （）</span><span class="sxs-lookup"><span data-stu-id="ff4bd-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ProductResource</span></span>

## <span data-ttu-id="ff4bd-135">筆記</span><span class="sxs-lookup"><span data-stu-id="ff4bd-135">NOTES</span></span>

## <span data-ttu-id="ff4bd-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="ff4bd-136">RELATED LINKS</span></span>
