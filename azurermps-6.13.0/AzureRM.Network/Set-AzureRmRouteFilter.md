---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
ms.openlocfilehash: 5dc2b6a9650cdf4110858edf1b061f69adac48f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624364"
---
# <span data-ttu-id="806f3-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="806f3-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="806f3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="806f3-102">SYNOPSIS</span></span>
<span data-ttu-id="806f3-103">{{填入摘要}}</span><span class="sxs-lookup"><span data-stu-id="806f3-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="806f3-104">句法</span><span class="sxs-lookup"><span data-stu-id="806f3-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="806f3-105">說明</span><span class="sxs-lookup"><span data-stu-id="806f3-105">DESCRIPTION</span></span>
<span data-ttu-id="806f3-106">{{填入描述}}</span><span class="sxs-lookup"><span data-stu-id="806f3-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="806f3-107">示例</span><span class="sxs-lookup"><span data-stu-id="806f3-107">EXAMPLES</span></span>

### <span data-ttu-id="806f3-108">範例1</span><span class="sxs-lookup"><span data-stu-id="806f3-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="806f3-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="806f3-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="806f3-110">參數</span><span class="sxs-lookup"><span data-stu-id="806f3-110">PARAMETERS</span></span>

### <span data-ttu-id="806f3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="806f3-111">-AsJob</span></span>
<span data-ttu-id="806f3-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="806f3-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="806f3-113">-DefaultProfile</span></span>
<span data-ttu-id="806f3-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="806f3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806f3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="806f3-115">-Force</span></span>
<span data-ttu-id="806f3-116">如果您想要 overrite 資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="806f3-116">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806f3-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="806f3-117">-RouteFilter</span></span>
<span data-ttu-id="806f3-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="806f3-118">The RouteFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="806f3-119">-確認</span><span class="sxs-lookup"><span data-stu-id="806f3-119">-Confirm</span></span>
<span data-ttu-id="806f3-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="806f3-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806f3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="806f3-121">-WhatIf</span></span>
<span data-ttu-id="806f3-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="806f3-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="806f3-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="806f3-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806f3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="806f3-124">CommonParameters</span></span>
<span data-ttu-id="806f3-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="806f3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="806f3-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="806f3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="806f3-127">輸入</span><span class="sxs-lookup"><span data-stu-id="806f3-127">INPUTS</span></span>

### <span data-ttu-id="806f3-128">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="806f3-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>
<span data-ttu-id="806f3-129">參數： RouteFilter (ByValue) </span><span class="sxs-lookup"><span data-stu-id="806f3-129">Parameters: RouteFilter (ByValue)</span></span>

## <span data-ttu-id="806f3-130">輸出</span><span class="sxs-lookup"><span data-stu-id="806f3-130">OUTPUTS</span></span>

### <span data-ttu-id="806f3-131">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="806f3-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="806f3-132">筆記</span><span class="sxs-lookup"><span data-stu-id="806f3-132">NOTES</span></span>

## <span data-ttu-id="806f3-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="806f3-133">RELATED LINKS</span></span>