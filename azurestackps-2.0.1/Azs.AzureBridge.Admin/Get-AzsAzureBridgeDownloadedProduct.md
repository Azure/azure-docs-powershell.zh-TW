---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 48b7cc2211df4fd8b9d65c3e93483a485a10ae32
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/26/2020
ms.locfileid: "93968786"
---
# <span data-ttu-id="9b416-101">Get-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="9b416-101">Get-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="9b416-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b416-102">SYNOPSIS</span></span>
<span data-ttu-id="9b416-103">傳回從 Azure MarketPlace 下載的產品清單。</span><span class="sxs-lookup"><span data-stu-id="9b416-103">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="9b416-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b416-104">SYNTAX</span></span>

### <span data-ttu-id="9b416-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="9b416-105">List (Default)</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="9b416-106">獲取</span><span class="sxs-lookup"><span data-stu-id="9b416-106">Get</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="9b416-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b416-107">ResourceId</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="9b416-108">說明</span><span class="sxs-lookup"><span data-stu-id="9b416-108">DESCRIPTION</span></span>
<span data-ttu-id="9b416-109">傳回從 Azure MarketPlace 下載的產品清單。</span><span class="sxs-lookup"><span data-stu-id="9b416-109">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="9b416-110">示例</span><span class="sxs-lookup"><span data-stu-id="9b416-110">EXAMPLES</span></span>

### <span data-ttu-id="9b416-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9b416-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="9b416-112">取得 Azure Bridge 已下載產品的清單</span><span class="sxs-lookup"><span data-stu-id="9b416-112">Get a list of Azure Bridge Downloaded products</span></span>

### <span data-ttu-id="9b416-113">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="9b416-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name 'microsoft.docker-arm.1.1.0' -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="9b416-114">透過名稱取得 Azure Bridge 已下載產品</span><span class="sxs-lookup"><span data-stu-id="9b416-114">Get an Azure Bridge Downloaded Product by Name</span></span>

## <span data-ttu-id="9b416-115">參數</span><span class="sxs-lookup"><span data-stu-id="9b416-115">PARAMETERS</span></span>

### <span data-ttu-id="9b416-116">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="9b416-116">-ActivationName</span></span>
<span data-ttu-id="9b416-117">啟用的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b416-117">Name of the activation.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b416-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="9b416-118">-Name</span></span>
<span data-ttu-id="9b416-119">產品名稱。</span><span class="sxs-lookup"><span data-stu-id="9b416-119">Name of the product.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b416-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b416-120">-ResourceGroupName</span></span>
<span data-ttu-id="9b416-121">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="9b416-121">The resource group the resource is located under.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b416-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b416-122">-ResourceId</span></span>
<span data-ttu-id="9b416-123">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="9b416-123">The resource id.</span></span>

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

### <span data-ttu-id="9b416-124">-略過</span><span class="sxs-lookup"><span data-stu-id="9b416-124">-Skip</span></span>
<span data-ttu-id="9b416-125">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="9b416-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="9b416-126">-上方</span><span class="sxs-lookup"><span data-stu-id="9b416-126">-Top</span></span>
<span data-ttu-id="9b416-127">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="9b416-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="9b416-128">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="9b416-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="9b416-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b416-129">CommonParameters</span></span>
<span data-ttu-id="9b416-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9b416-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b416-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9b416-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b416-132">輸入</span><span class="sxs-lookup"><span data-stu-id="9b416-132">INPUTS</span></span>

## <span data-ttu-id="9b416-133">輸出</span><span class="sxs-lookup"><span data-stu-id="9b416-133">OUTPUTS</span></span>

### <span data-ttu-id="9b416-134">AzureStack AzureBridge. DownloadedProductResource （）</span><span class="sxs-lookup"><span data-stu-id="9b416-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="9b416-135">筆記</span><span class="sxs-lookup"><span data-stu-id="9b416-135">NOTES</span></span>

## <span data-ttu-id="9b416-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b416-136">RELATED LINKS</span></span>

