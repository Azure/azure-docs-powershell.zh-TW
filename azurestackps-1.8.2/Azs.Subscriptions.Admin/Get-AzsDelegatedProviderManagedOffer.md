---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: edf7b9135bc1f2d614f9fc516acadbc31821c45e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968355"
---
# <span data-ttu-id="29ef3-101">Get-AzsDelegatedProviderManagedOffer</span><span class="sxs-lookup"><span data-stu-id="29ef3-101">Get-AzsDelegatedProviderManagedOffer</span></span>

## <span data-ttu-id="29ef3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="29ef3-102">SYNOPSIS</span></span>
<span data-ttu-id="29ef3-103">取得委派提供者的提供方案清單。</span><span class="sxs-lookup"><span data-stu-id="29ef3-103">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="29ef3-104">句法</span><span class="sxs-lookup"><span data-stu-id="29ef3-104">SYNTAX</span></span>

### <span data-ttu-id="29ef3-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="29ef3-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="29ef3-106">獲取</span><span class="sxs-lookup"><span data-stu-id="29ef3-106">Get</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="29ef3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="29ef3-107">ResourceId</span></span>
```
Get-AzsDelegatedProviderManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="29ef3-108">說明</span><span class="sxs-lookup"><span data-stu-id="29ef3-108">DESCRIPTION</span></span>
<span data-ttu-id="29ef3-109">取得委派提供者的提供方案清單。</span><span class="sxs-lookup"><span data-stu-id="29ef3-109">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="29ef3-110">示例</span><span class="sxs-lookup"><span data-stu-id="29ef3-110">EXAMPLES</span></span>

### <span data-ttu-id="29ef3-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="29ef3-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProvider "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="29ef3-112">取得委派提供者的提供方案清單。</span><span class="sxs-lookup"><span data-stu-id="29ef3-112">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="29ef3-113">參數</span><span class="sxs-lookup"><span data-stu-id="29ef3-113">PARAMETERS</span></span>

### <span data-ttu-id="29ef3-114">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="29ef3-114">-DelegatedProviderId</span></span>
<span data-ttu-id="29ef3-115">DelegatedProvider 識別碼]。</span><span class="sxs-lookup"><span data-stu-id="29ef3-115">DelegatedProvider identifier.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: DelegatedProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ef3-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="29ef3-116">-Name</span></span>
<span data-ttu-id="29ef3-117">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="29ef3-117">Name of an offer.</span></span>

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

### <span data-ttu-id="29ef3-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29ef3-118">-ResourceId</span></span>
<span data-ttu-id="29ef3-119">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="29ef3-119">The resource id.</span></span>

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

### <span data-ttu-id="29ef3-120">-略過</span><span class="sxs-lookup"><span data-stu-id="29ef3-120">-Skip</span></span>
<span data-ttu-id="29ef3-121">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="29ef3-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="29ef3-122">-上方</span><span class="sxs-lookup"><span data-stu-id="29ef3-122">-Top</span></span>
<span data-ttu-id="29ef3-123">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="29ef3-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="29ef3-124">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="29ef3-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="29ef3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29ef3-125">CommonParameters</span></span>
<span data-ttu-id="29ef3-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="29ef3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29ef3-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="29ef3-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29ef3-128">輸入</span><span class="sxs-lookup"><span data-stu-id="29ef3-128">INPUTS</span></span>

## <span data-ttu-id="29ef3-129">輸出</span><span class="sxs-lookup"><span data-stu-id="29ef3-129">OUTPUTS</span></span>

### <span data-ttu-id="29ef3-130">AzureStack DelegatedProviderOffer 的訂閱。</span><span class="sxs-lookup"><span data-stu-id="29ef3-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DelegatedProviderOffer</span></span>

## <span data-ttu-id="29ef3-131">筆記</span><span class="sxs-lookup"><span data-stu-id="29ef3-131">NOTES</span></span>

## <span data-ttu-id="29ef3-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="29ef3-132">RELATED LINKS</span></span>

