---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 267a5bf4c3f864c987c0bc747eefce9dd3ffe6b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793069"
---
# <span data-ttu-id="5ab1e-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="5ab1e-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="5ab1e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ab1e-102">SYNOPSIS</span></span>
<span data-ttu-id="5ab1e-103">傳回指定訂閱資源類型和名稱的 avaialbility</span><span class="sxs-lookup"><span data-stu-id="5ab1e-103">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="5ab1e-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ab1e-104">SYNTAX</span></span>

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## <span data-ttu-id="5ab1e-105">說明</span><span class="sxs-lookup"><span data-stu-id="5ab1e-105">DESCRIPTION</span></span>
<span data-ttu-id="5ab1e-106">傳回指定訂閱資源類型和名稱的 avaialbility</span><span class="sxs-lookup"><span data-stu-id="5ab1e-106">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="5ab1e-107">示例</span><span class="sxs-lookup"><span data-stu-id="5ab1e-107">EXAMPLES</span></span>

### <span data-ttu-id="5ab1e-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5ab1e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

<span data-ttu-id="5ab1e-109">傳回指定訂閱資源類型和名稱的 avaialbility</span><span class="sxs-lookup"><span data-stu-id="5ab1e-109">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="5ab1e-110">參數</span><span class="sxs-lookup"><span data-stu-id="5ab1e-110">PARAMETERS</span></span>

### <span data-ttu-id="5ab1e-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="5ab1e-111">-Name</span></span>
<span data-ttu-id="5ab1e-112">要驗證的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="5ab1e-112">The resource name to verify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab1e-113">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="5ab1e-113">-ResourceType</span></span>
<span data-ttu-id="5ab1e-114">要驗證的資源類型。</span><span class="sxs-lookup"><span data-stu-id="5ab1e-114">The resource type to verify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab1e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ab1e-115">CommonParameters</span></span>
<span data-ttu-id="5ab1e-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ab1e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ab1e-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5ab1e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ab1e-118">輸入</span><span class="sxs-lookup"><span data-stu-id="5ab1e-118">INPUTS</span></span>

## <span data-ttu-id="5ab1e-119">輸出</span><span class="sxs-lookup"><span data-stu-id="5ab1e-119">OUTPUTS</span></span>

### <span data-ttu-id="5ab1e-120">AzureStack CheckNameAvailabilityResponse 的訂閱。</span><span class="sxs-lookup"><span data-stu-id="5ab1e-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.CheckNameAvailabilityResponse</span></span>

## <span data-ttu-id="5ab1e-121">筆記</span><span class="sxs-lookup"><span data-stu-id="5ab1e-121">NOTES</span></span>

## <span data-ttu-id="5ab1e-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ab1e-122">RELATED LINKS</span></span>

