---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: f5b2a3f66a1972edbf6d3e475f5f30fc9530929f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448095"
---
# <span data-ttu-id="d110f-101">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d110f-101">Set-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="d110f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d110f-102">SYNOPSIS</span></span>
<span data-ttu-id="d110f-103">{{填入摘要}}</span><span class="sxs-lookup"><span data-stu-id="d110f-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d110f-104">句法</span><span class="sxs-lookup"><span data-stu-id="d110f-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d110f-105">說明</span><span class="sxs-lookup"><span data-stu-id="d110f-105">DESCRIPTION</span></span>
<span data-ttu-id="d110f-106">{{填入描述}}</span><span class="sxs-lookup"><span data-stu-id="d110f-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="d110f-107">示例</span><span class="sxs-lookup"><span data-stu-id="d110f-107">EXAMPLES</span></span>

### <span data-ttu-id="d110f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d110f-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="d110f-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="d110f-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="d110f-110">參數</span><span class="sxs-lookup"><span data-stu-id="d110f-110">PARAMETERS</span></span>

### <span data-ttu-id="d110f-111">-Access</span><span class="sxs-lookup"><span data-stu-id="d110f-111">-Access</span></span>
<span data-ttu-id="d110f-112">規則的存取類型。</span><span class="sxs-lookup"><span data-stu-id="d110f-112">The access type of the rule.</span></span>
<span data-ttu-id="d110f-113">可能的值為： "Allow"，"Deny"</span><span class="sxs-lookup"><span data-stu-id="d110f-113">Possible values are: 'Allow', 'Deny'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d110f-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="d110f-114">-CommunityList</span></span>
<span data-ttu-id="d110f-115">路由篩選將篩選的群組值清單</span><span class="sxs-lookup"><span data-stu-id="d110f-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="d110f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d110f-116">-Force</span></span>
<span data-ttu-id="d110f-117">如果您想要 overrite 資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="d110f-117">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="d110f-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="d110f-118">-Name</span></span>
<span data-ttu-id="d110f-119">路由篩選規則的名稱</span><span class="sxs-lookup"><span data-stu-id="d110f-119">The name of the route filter rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d110f-120">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="d110f-120">-RouteFilter</span></span>
<span data-ttu-id="d110f-121">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="d110f-121">The RouteFilter</span></span>

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

### <span data-ttu-id="d110f-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="d110f-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="d110f-123">規則的路由篩選規則類型。</span><span class="sxs-lookup"><span data-stu-id="d110f-123">The route filter rule type of the rule.</span></span>
<span data-ttu-id="d110f-124">可能的值為： "社團"</span><span class="sxs-lookup"><span data-stu-id="d110f-124">Possible values are: 'Community'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d110f-125">-確認</span><span class="sxs-lookup"><span data-stu-id="d110f-125">-Confirm</span></span>
<span data-ttu-id="d110f-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d110f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d110f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d110f-127">-WhatIf</span></span>
<span data-ttu-id="d110f-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d110f-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d110f-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d110f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d110f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d110f-130">-DefaultProfile</span></span>
<span data-ttu-id="d110f-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d110f-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d110f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d110f-132">CommonParameters</span></span>
<span data-ttu-id="d110f-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d110f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d110f-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d110f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d110f-135">輸入</span><span class="sxs-lookup"><span data-stu-id="d110f-135">INPUTS</span></span>

### <span data-ttu-id="d110f-136">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d110f-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="d110f-137">輸出</span><span class="sxs-lookup"><span data-stu-id="d110f-137">OUTPUTS</span></span>

### <span data-ttu-id="d110f-138">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d110f-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="d110f-139">筆記</span><span class="sxs-lookup"><span data-stu-id="d110f-139">NOTES</span></span>

## <span data-ttu-id="d110f-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="d110f-140">RELATED LINKS</span></span>

