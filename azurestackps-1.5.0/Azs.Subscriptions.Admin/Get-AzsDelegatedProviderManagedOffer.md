---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 57e195f1d42b4d1df26344133c10d7c0d40e1f8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442475"
---
# <span data-ttu-id="12e10-101">Get-AzsDelegatedProviderManagedOffer</span><span class="sxs-lookup"><span data-stu-id="12e10-101">Get-AzsDelegatedProviderManagedOffer</span></span>

## <span data-ttu-id="12e10-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12e10-102">SYNOPSIS</span></span>
<span data-ttu-id="12e10-103">取得委派提供者的提供方案清單。</span><span class="sxs-lookup"><span data-stu-id="12e10-103">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="12e10-104">句法</span><span class="sxs-lookup"><span data-stu-id="12e10-104">SYNTAX</span></span>

### <span data-ttu-id="12e10-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="12e10-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="12e10-106">獲取</span><span class="sxs-lookup"><span data-stu-id="12e10-106">Get</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="12e10-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="12e10-107">ResourceId</span></span>
```
Get-AzsDelegatedProviderManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="12e10-108">說明</span><span class="sxs-lookup"><span data-stu-id="12e10-108">DESCRIPTION</span></span>
<span data-ttu-id="12e10-109">取得委派提供者的提供方案清單。</span><span class="sxs-lookup"><span data-stu-id="12e10-109">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="12e10-110">示例</span><span class="sxs-lookup"><span data-stu-id="12e10-110">EXAMPLES</span></span>

### <span data-ttu-id="12e10-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="12e10-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProvider "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="12e10-112">取得委派提供者的提供方案清單。</span><span class="sxs-lookup"><span data-stu-id="12e10-112">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="12e10-113">參數</span><span class="sxs-lookup"><span data-stu-id="12e10-113">PARAMETERS</span></span>

### <span data-ttu-id="12e10-114">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="12e10-114">-DelegatedProviderId</span></span>
<span data-ttu-id="12e10-115">DelegatedProvider 識別碼]。</span><span class="sxs-lookup"><span data-stu-id="12e10-115">DelegatedProvider identifier.</span></span>

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

### <span data-ttu-id="12e10-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="12e10-116">-Name</span></span>
<span data-ttu-id="12e10-117">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="12e10-117">Name of an offer.</span></span>

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

### <span data-ttu-id="12e10-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12e10-118">-ResourceId</span></span>
<span data-ttu-id="12e10-119">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="12e10-119">The resource id.</span></span>

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

### <span data-ttu-id="12e10-120">-略過</span><span class="sxs-lookup"><span data-stu-id="12e10-120">-Skip</span></span>
<span data-ttu-id="12e10-121">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="12e10-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="12e10-122">-上方</span><span class="sxs-lookup"><span data-stu-id="12e10-122">-Top</span></span>
<span data-ttu-id="12e10-123">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="12e10-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="12e10-124">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="12e10-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="12e10-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e10-125">CommonParameters</span></span>
<span data-ttu-id="12e10-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12e10-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e10-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="12e10-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e10-128">輸入</span><span class="sxs-lookup"><span data-stu-id="12e10-128">INPUTS</span></span>

## <span data-ttu-id="12e10-129">輸出</span><span class="sxs-lookup"><span data-stu-id="12e10-129">OUTPUTS</span></span>

### <span data-ttu-id="12e10-130">AzureStack DelegatedProviderOffer 的訂閱。</span><span class="sxs-lookup"><span data-stu-id="12e10-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DelegatedProviderOffer</span></span>

## <span data-ttu-id="12e10-131">筆記</span><span class="sxs-lookup"><span data-stu-id="12e10-131">NOTES</span></span>

## <span data-ttu-id="12e10-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="12e10-132">RELATED LINKS</span></span>

