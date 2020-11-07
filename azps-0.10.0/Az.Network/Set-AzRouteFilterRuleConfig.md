---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 8ab95789b73623716edc818c8092c8c0cd58c534
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795390"
---
# <span data-ttu-id="01349-101">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="01349-101">Set-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="01349-102">摘要</span><span class="sxs-lookup"><span data-stu-id="01349-102">SYNOPSIS</span></span>
<span data-ttu-id="01349-103">{{填入摘要}}</span><span class="sxs-lookup"><span data-stu-id="01349-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="01349-104">句法</span><span class="sxs-lookup"><span data-stu-id="01349-104">SYNTAX</span></span>

```
Set-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01349-105">說明</span><span class="sxs-lookup"><span data-stu-id="01349-105">DESCRIPTION</span></span>
<span data-ttu-id="01349-106">{{填入描述}}</span><span class="sxs-lookup"><span data-stu-id="01349-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="01349-107">示例</span><span class="sxs-lookup"><span data-stu-id="01349-107">EXAMPLES</span></span>

### <span data-ttu-id="01349-108">範例1</span><span class="sxs-lookup"><span data-stu-id="01349-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="01349-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="01349-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="01349-110">參數</span><span class="sxs-lookup"><span data-stu-id="01349-110">PARAMETERS</span></span>

### <span data-ttu-id="01349-111">-Access</span><span class="sxs-lookup"><span data-stu-id="01349-111">-Access</span></span>
<span data-ttu-id="01349-112">規則的存取類型。</span><span class="sxs-lookup"><span data-stu-id="01349-112">The access type of the rule.</span></span>
<span data-ttu-id="01349-113">可能的值為： "Allow"，"Deny"</span><span class="sxs-lookup"><span data-stu-id="01349-113">Possible values are: 'Allow', 'Deny'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01349-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="01349-114">-CommunityList</span></span>
<span data-ttu-id="01349-115">路由篩選將篩選的群組值清單</span><span class="sxs-lookup"><span data-stu-id="01349-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01349-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01349-116">-DefaultProfile</span></span>
<span data-ttu-id="01349-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="01349-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01349-118">-Force</span><span class="sxs-lookup"><span data-stu-id="01349-118">-Force</span></span>
<span data-ttu-id="01349-119">如果您想要 overrite 資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="01349-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="01349-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="01349-120">-Name</span></span>
<span data-ttu-id="01349-121">路由篩選規則的名稱</span><span class="sxs-lookup"><span data-stu-id="01349-121">The name of the route filter rule</span></span>

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

### <span data-ttu-id="01349-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="01349-122">-RouteFilter</span></span>
<span data-ttu-id="01349-123">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="01349-123">The RouteFilter</span></span>

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

### <span data-ttu-id="01349-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="01349-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="01349-125">規則的路由篩選規則類型。</span><span class="sxs-lookup"><span data-stu-id="01349-125">The route filter rule type of the rule.</span></span>
<span data-ttu-id="01349-126">可能的值為： "社團"</span><span class="sxs-lookup"><span data-stu-id="01349-126">Possible values are: 'Community'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01349-127">-確認</span><span class="sxs-lookup"><span data-stu-id="01349-127">-Confirm</span></span>
<span data-ttu-id="01349-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="01349-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01349-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01349-129">-WhatIf</span></span>
<span data-ttu-id="01349-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="01349-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01349-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="01349-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01349-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01349-132">CommonParameters</span></span>
<span data-ttu-id="01349-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="01349-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01349-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="01349-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01349-135">輸入</span><span class="sxs-lookup"><span data-stu-id="01349-135">INPUTS</span></span>

### <span data-ttu-id="01349-136">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="01349-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="01349-137">輸出</span><span class="sxs-lookup"><span data-stu-id="01349-137">OUTPUTS</span></span>

### <span data-ttu-id="01349-138">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="01349-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="01349-139">筆記</span><span class="sxs-lookup"><span data-stu-id="01349-139">NOTES</span></span>

## <span data-ttu-id="01349-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="01349-140">RELATED LINKS</span></span>

