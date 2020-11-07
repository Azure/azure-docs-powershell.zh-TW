---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilter
schema: 2.0.0
ms.openlocfilehash: 895819175f9fe4215d926d57c55307bbb4c75ab3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801946"
---
# <span data-ttu-id="74af7-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="74af7-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="74af7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74af7-102">SYNOPSIS</span></span>
<span data-ttu-id="74af7-103">{{填入摘要}}</span><span class="sxs-lookup"><span data-stu-id="74af7-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74af7-104">句法</span><span class="sxs-lookup"><span data-stu-id="74af7-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74af7-105">說明</span><span class="sxs-lookup"><span data-stu-id="74af7-105">DESCRIPTION</span></span>
<span data-ttu-id="74af7-106">{{填入描述}}</span><span class="sxs-lookup"><span data-stu-id="74af7-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="74af7-107">示例</span><span class="sxs-lookup"><span data-stu-id="74af7-107">EXAMPLES</span></span>

### <span data-ttu-id="74af7-108">範例1</span><span class="sxs-lookup"><span data-stu-id="74af7-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="74af7-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="74af7-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="74af7-110">參數</span><span class="sxs-lookup"><span data-stu-id="74af7-110">PARAMETERS</span></span>

### <span data-ttu-id="74af7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74af7-111">-AsJob</span></span>
<span data-ttu-id="74af7-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="74af7-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74af7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74af7-113">-DefaultProfile</span></span>
<span data-ttu-id="74af7-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="74af7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74af7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="74af7-115">-Force</span></span>
<span data-ttu-id="74af7-116">如果您想要 overrite 資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="74af7-116">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74af7-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="74af7-117">-RouteFilter</span></span>
<span data-ttu-id="74af7-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="74af7-118">The RouteFilter</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74af7-119">-確認</span><span class="sxs-lookup"><span data-stu-id="74af7-119">-Confirm</span></span>
<span data-ttu-id="74af7-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="74af7-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74af7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74af7-121">-WhatIf</span></span>
<span data-ttu-id="74af7-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="74af7-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74af7-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="74af7-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74af7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74af7-124">CommonParameters</span></span>
<span data-ttu-id="74af7-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74af7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74af7-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="74af7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74af7-127">輸入</span><span class="sxs-lookup"><span data-stu-id="74af7-127">INPUTS</span></span>

### <span data-ttu-id="74af7-128">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="74af7-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="74af7-129">輸出</span><span class="sxs-lookup"><span data-stu-id="74af7-129">OUTPUTS</span></span>

### <span data-ttu-id="74af7-130">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="74af7-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="74af7-131">筆記</span><span class="sxs-lookup"><span data-stu-id="74af7-131">NOTES</span></span>

## <span data-ttu-id="74af7-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="74af7-132">RELATED LINKS</span></span>

