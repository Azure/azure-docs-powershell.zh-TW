---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88c19285ee7188dab272eeab7a668f5f5dfe22a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443220"
---
# <span data-ttu-id="7f932-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="7f932-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="7f932-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7f932-102">SYNOPSIS</span></span>
<span data-ttu-id="7f932-103">取得 delegatedProviders 清單。</span><span class="sxs-lookup"><span data-stu-id="7f932-103">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="7f932-104">句法</span><span class="sxs-lookup"><span data-stu-id="7f932-104">SYNTAX</span></span>

### <span data-ttu-id="7f932-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="7f932-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### <span data-ttu-id="7f932-106">獲取</span><span class="sxs-lookup"><span data-stu-id="7f932-106">Get</span></span>
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## <span data-ttu-id="7f932-107">說明</span><span class="sxs-lookup"><span data-stu-id="7f932-107">DESCRIPTION</span></span>
<span data-ttu-id="7f932-108">取得 delegatedProviders 清單。</span><span class="sxs-lookup"><span data-stu-id="7f932-108">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="7f932-109">示例</span><span class="sxs-lookup"><span data-stu-id="7f932-109">EXAMPLES</span></span>

### <span data-ttu-id="7f932-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7f932-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProvider
```

<span data-ttu-id="7f932-111">取得委派提供者的清單。</span><span class="sxs-lookup"><span data-stu-id="7f932-111">Get a list of delegated providers.</span></span>

### <span data-ttu-id="7f932-112">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="7f932-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="7f932-113">取得特定的委派提供者。</span><span class="sxs-lookup"><span data-stu-id="7f932-113">Get the a specific delegated provider.</span></span>

## <span data-ttu-id="7f932-114">參數</span><span class="sxs-lookup"><span data-stu-id="7f932-114">PARAMETERS</span></span>

### <span data-ttu-id="7f932-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="7f932-115">-DelegatedProviderId</span></span>
<span data-ttu-id="7f932-116">DelegatedProvider 識別碼]。</span><span class="sxs-lookup"><span data-stu-id="7f932-116">DelegatedProvider identifier.</span></span>

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

### <span data-ttu-id="7f932-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f932-117">CommonParameters</span></span>
<span data-ttu-id="7f932-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7f932-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f932-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7f932-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f932-120">輸入</span><span class="sxs-lookup"><span data-stu-id="7f932-120">INPUTS</span></span>

## <span data-ttu-id="7f932-121">輸出</span><span class="sxs-lookup"><span data-stu-id="7f932-121">OUTPUTS</span></span>

### <span data-ttu-id="7f932-122">AzureStack. 系統管理. 訂閱</span><span class="sxs-lookup"><span data-stu-id="7f932-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="7f932-123">筆記</span><span class="sxs-lookup"><span data-stu-id="7f932-123">NOTES</span></span>

## <span data-ttu-id="7f932-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f932-124">RELATED LINKS</span></span>

