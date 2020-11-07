---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
ms.openlocfilehash: bcb0d59c564087e02cd152c1ae76f38c91f33e80
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795489"
---
# <span data-ttu-id="3ae63-101">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3ae63-101">Remove-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="3ae63-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3ae63-102">SYNOPSIS</span></span>
<span data-ttu-id="3ae63-103">{{填入摘要}}</span><span class="sxs-lookup"><span data-stu-id="3ae63-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="3ae63-104">句法</span><span class="sxs-lookup"><span data-stu-id="3ae63-104">SYNTAX</span></span>

```
Remove-AzRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ae63-105">說明</span><span class="sxs-lookup"><span data-stu-id="3ae63-105">DESCRIPTION</span></span>
<span data-ttu-id="3ae63-106">{{填入描述}}</span><span class="sxs-lookup"><span data-stu-id="3ae63-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="3ae63-107">示例</span><span class="sxs-lookup"><span data-stu-id="3ae63-107">EXAMPLES</span></span>

### <span data-ttu-id="3ae63-108">範例1</span><span class="sxs-lookup"><span data-stu-id="3ae63-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="3ae63-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="3ae63-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="3ae63-110">參數</span><span class="sxs-lookup"><span data-stu-id="3ae63-110">PARAMETERS</span></span>

### <span data-ttu-id="3ae63-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ae63-111">-DefaultProfile</span></span>
<span data-ttu-id="3ae63-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3ae63-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ae63-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3ae63-113">-Force</span></span>
<span data-ttu-id="3ae63-114">如果您想要 overrite 資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="3ae63-114">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="3ae63-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="3ae63-115">-Name</span></span>
<span data-ttu-id="3ae63-116">路由篩選規則的名稱</span><span class="sxs-lookup"><span data-stu-id="3ae63-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="3ae63-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="3ae63-117">-RouteFilter</span></span>
<span data-ttu-id="3ae63-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="3ae63-118">The RouteFilter</span></span>

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

### <span data-ttu-id="3ae63-119">-確認</span><span class="sxs-lookup"><span data-stu-id="3ae63-119">-Confirm</span></span>
<span data-ttu-id="3ae63-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3ae63-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ae63-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ae63-121">-WhatIf</span></span>
<span data-ttu-id="3ae63-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3ae63-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ae63-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3ae63-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ae63-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ae63-124">CommonParameters</span></span>
<span data-ttu-id="3ae63-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3ae63-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ae63-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3ae63-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ae63-127">輸入</span><span class="sxs-lookup"><span data-stu-id="3ae63-127">INPUTS</span></span>

### <span data-ttu-id="3ae63-128">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3ae63-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="3ae63-129">輸出</span><span class="sxs-lookup"><span data-stu-id="3ae63-129">OUTPUTS</span></span>

### <span data-ttu-id="3ae63-130">PSRouteFilterRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3ae63-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="3ae63-131">筆記</span><span class="sxs-lookup"><span data-stu-id="3ae63-131">NOTES</span></span>

## <span data-ttu-id="3ae63-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ae63-132">RELATED LINKS</span></span>

