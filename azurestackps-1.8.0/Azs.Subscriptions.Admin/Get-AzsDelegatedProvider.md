---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: afc99afebed095da96d826918cc6912f197d1899
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793669"
---
# <span data-ttu-id="bc1f0-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="bc1f0-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="bc1f0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bc1f0-102">SYNOPSIS</span></span>
<span data-ttu-id="bc1f0-103">取得 delegatedProviders 清單。</span><span class="sxs-lookup"><span data-stu-id="bc1f0-103">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="bc1f0-104">句法</span><span class="sxs-lookup"><span data-stu-id="bc1f0-104">SYNTAX</span></span>

### <span data-ttu-id="bc1f0-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="bc1f0-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### <span data-ttu-id="bc1f0-106">獲取</span><span class="sxs-lookup"><span data-stu-id="bc1f0-106">Get</span></span>
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## <span data-ttu-id="bc1f0-107">說明</span><span class="sxs-lookup"><span data-stu-id="bc1f0-107">DESCRIPTION</span></span>
<span data-ttu-id="bc1f0-108">取得 delegatedProviders 清單。</span><span class="sxs-lookup"><span data-stu-id="bc1f0-108">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="bc1f0-109">示例</span><span class="sxs-lookup"><span data-stu-id="bc1f0-109">EXAMPLES</span></span>

### <span data-ttu-id="bc1f0-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bc1f0-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProvider
```

<span data-ttu-id="bc1f0-111">取得委派提供者的清單。</span><span class="sxs-lookup"><span data-stu-id="bc1f0-111">Get a list of delegated providers.</span></span>

### <span data-ttu-id="bc1f0-112">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="bc1f0-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="bc1f0-113">取得特定的委派提供者。</span><span class="sxs-lookup"><span data-stu-id="bc1f0-113">Get the a specific delegated provider.</span></span>

## <span data-ttu-id="bc1f0-114">參數</span><span class="sxs-lookup"><span data-stu-id="bc1f0-114">PARAMETERS</span></span>

### <span data-ttu-id="bc1f0-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="bc1f0-115">-DelegatedProviderId</span></span>
<span data-ttu-id="bc1f0-116">{{Fill DelegatedProviderId 說明}}</span><span class="sxs-lookup"><span data-stu-id="bc1f0-116">{{Fill DelegatedProviderId Description}}</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc1f0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc1f0-117">CommonParameters</span></span>
<span data-ttu-id="bc1f0-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bc1f0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc1f0-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bc1f0-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc1f0-120">輸入</span><span class="sxs-lookup"><span data-stu-id="bc1f0-120">INPUTS</span></span>

## <span data-ttu-id="bc1f0-121">輸出</span><span class="sxs-lookup"><span data-stu-id="bc1f0-121">OUTPUTS</span></span>

### <span data-ttu-id="bc1f0-122">AzureStack. 系統管理. 訂閱</span><span class="sxs-lookup"><span data-stu-id="bc1f0-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="bc1f0-123">筆記</span><span class="sxs-lookup"><span data-stu-id="bc1f0-123">NOTES</span></span>

## <span data-ttu-id="bc1f0-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="bc1f0-124">RELATED LINKS</span></span>

