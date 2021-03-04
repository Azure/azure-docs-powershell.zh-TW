---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.DigitalTwins/new-AzDigitalTwinsDigitalTwinsIdentityObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
ms.openlocfilehash: 2b038699dfa1cd959ea20b761b6c24dee69a9e49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910185"
---
# <span data-ttu-id="d151b-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="d151b-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span></span>

## <span data-ttu-id="d151b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d151b-102">SYNOPSIS</span></span>
<span data-ttu-id="d151b-103">為 DigitalTwinsIdentity 建立記憶體中的物件</span><span class="sxs-lookup"><span data-stu-id="d151b-103">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="d151b-104">語法</span><span class="sxs-lookup"><span data-stu-id="d151b-104">SYNTAX</span></span>

```
New-AzDigitalTwinsDigitalTwinsIdentityObject [-EndpointName <String>] [-Id <String>] [-Location <String>]
 [-ResourceGroupName <String>] [-ResourceName <String>] [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="d151b-105">描述</span><span class="sxs-lookup"><span data-stu-id="d151b-105">DESCRIPTION</span></span>
<span data-ttu-id="d151b-106">為 DigitalTwinsIdentity 建立記憶體中的物件</span><span class="sxs-lookup"><span data-stu-id="d151b-106">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="d151b-107">例子</span><span class="sxs-lookup"><span data-stu-id="d151b-107">EXAMPLES</span></span>

### <span data-ttu-id="d151b-108">範例 1：建立 DigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="d151b-108">Example 1: Create A DigitalTwinsIdentityObject</span></span>
```powershell
PS C:\> New-AzDigitalTwinsDigitalTwinsIdentityObject -Id '************' -Location eastus

EndpointName Location ResourceGroupName ResourceName SubscriptionId
------------ -------- ----------------- ------------ --------------
             eastus
```

<span data-ttu-id="d151b-109">根據識別碼和位置建立 DigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="d151b-109">Create A DigitalTwinsIdentityObject by Id and location</span></span>

## <span data-ttu-id="d151b-110">參數</span><span class="sxs-lookup"><span data-stu-id="d151b-110">PARAMETERS</span></span>

### <span data-ttu-id="d151b-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d151b-111">-EndpointName</span></span>
<span data-ttu-id="d151b-112">端點資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="d151b-112">Name of Endpoint Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d151b-113">-Id</span><span class="sxs-lookup"><span data-stu-id="d151b-113">-Id</span></span>
<span data-ttu-id="d151b-114">資源識別路徑。</span><span class="sxs-lookup"><span data-stu-id="d151b-114">Resource identity path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d151b-115">-位置</span><span class="sxs-lookup"><span data-stu-id="d151b-115">-Location</span></span>
<span data-ttu-id="d151b-116">DigitalTwinsInstance 的位置。</span><span class="sxs-lookup"><span data-stu-id="d151b-116">Location of DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d151b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d151b-117">-ResourceGroupName</span></span>
<span data-ttu-id="d151b-118">包含 DigitalTwinsInstance 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="d151b-118">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d151b-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d151b-119">-ResourceName</span></span>
<span data-ttu-id="d151b-120">DigitalTwinsInstance 的名稱。</span><span class="sxs-lookup"><span data-stu-id="d151b-120">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d151b-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d151b-121">-SubscriptionId</span></span>
<span data-ttu-id="d151b-122">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="d151b-122">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d151b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d151b-123">CommonParameters</span></span>
<span data-ttu-id="d151b-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d151b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d151b-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d151b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d151b-126">輸入</span><span class="sxs-lookup"><span data-stu-id="d151b-126">INPUTS</span></span>

## <span data-ttu-id="d151b-127">輸出</span><span class="sxs-lookup"><span data-stu-id="d151b-127">OUTPUTS</span></span>

### <span data-ttu-id="d151b-128">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.models.DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="d151b-128">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.DigitalTwinsIdentity</span></span>

## <span data-ttu-id="d151b-129">筆記</span><span class="sxs-lookup"><span data-stu-id="d151b-129">NOTES</span></span>

<span data-ttu-id="d151b-130">別名</span><span class="sxs-lookup"><span data-stu-id="d151b-130">ALIASES</span></span>

## <span data-ttu-id="d151b-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="d151b-131">RELATED LINKS</span></span>

