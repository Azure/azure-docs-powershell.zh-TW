---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4bd00dc1709a3060da9777ab4755ae1c6a28ec4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93794018"
---
# <span data-ttu-id="40f28-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="40f28-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="40f28-102">摘要</span><span class="sxs-lookup"><span data-stu-id="40f28-102">SYNOPSIS</span></span>
<span data-ttu-id="40f28-103">傳回指定訂閱資源類型和名稱的 avaialbility</span><span class="sxs-lookup"><span data-stu-id="40f28-103">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="40f28-104">句法</span><span class="sxs-lookup"><span data-stu-id="40f28-104">SYNTAX</span></span>

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## <span data-ttu-id="40f28-105">說明</span><span class="sxs-lookup"><span data-stu-id="40f28-105">DESCRIPTION</span></span>
<span data-ttu-id="40f28-106">傳回指定訂閱資源類型和名稱的 avaialbility</span><span class="sxs-lookup"><span data-stu-id="40f28-106">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="40f28-107">示例</span><span class="sxs-lookup"><span data-stu-id="40f28-107">EXAMPLES</span></span>

### <span data-ttu-id="40f28-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="40f28-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

<span data-ttu-id="40f28-109">傳回指定訂閱資源類型和名稱的 avaialbility</span><span class="sxs-lookup"><span data-stu-id="40f28-109">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="40f28-110">參數</span><span class="sxs-lookup"><span data-stu-id="40f28-110">PARAMETERS</span></span>

### <span data-ttu-id="40f28-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="40f28-111">-Name</span></span>
<span data-ttu-id="40f28-112">要驗證的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="40f28-112">The resource name to verify.</span></span>

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

### <span data-ttu-id="40f28-113">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="40f28-113">-ResourceType</span></span>
<span data-ttu-id="40f28-114">要驗證的資源類型。</span><span class="sxs-lookup"><span data-stu-id="40f28-114">The resource type to verify.</span></span>

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

### <span data-ttu-id="40f28-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40f28-115">CommonParameters</span></span>
<span data-ttu-id="40f28-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="40f28-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40f28-117">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="40f28-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40f28-118">輸入</span><span class="sxs-lookup"><span data-stu-id="40f28-118">INPUTS</span></span>

## <span data-ttu-id="40f28-119">輸出</span><span class="sxs-lookup"><span data-stu-id="40f28-119">OUTPUTS</span></span>

### <span data-ttu-id="40f28-120">AzureStack CheckNameAvailabilityResponse 的訂閱。</span><span class="sxs-lookup"><span data-stu-id="40f28-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.CheckNameAvailabilityResponse</span></span>

## <span data-ttu-id="40f28-121">筆記</span><span class="sxs-lookup"><span data-stu-id="40f28-121">NOTES</span></span>

## <span data-ttu-id="40f28-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="40f28-122">RELATED LINKS</span></span>

