---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: d73fbe14e4b1d4c4ea34c7405ad7da5b7954ffd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454888"
---
# <span data-ttu-id="29ec7-101">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="29ec7-101">Remove-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="29ec7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="29ec7-102">SYNOPSIS</span></span>
<span data-ttu-id="29ec7-103">{{填入摘要}}</span><span class="sxs-lookup"><span data-stu-id="29ec7-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29ec7-104">句法</span><span class="sxs-lookup"><span data-stu-id="29ec7-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29ec7-105">說明</span><span class="sxs-lookup"><span data-stu-id="29ec7-105">DESCRIPTION</span></span>
<span data-ttu-id="29ec7-106">{{填入描述}}</span><span class="sxs-lookup"><span data-stu-id="29ec7-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="29ec7-107">示例</span><span class="sxs-lookup"><span data-stu-id="29ec7-107">EXAMPLES</span></span>

### <span data-ttu-id="29ec7-108">範例1</span><span class="sxs-lookup"><span data-stu-id="29ec7-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="29ec7-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="29ec7-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="29ec7-110">參數</span><span class="sxs-lookup"><span data-stu-id="29ec7-110">PARAMETERS</span></span>

### <span data-ttu-id="29ec7-111">-Force</span><span class="sxs-lookup"><span data-stu-id="29ec7-111">-Force</span></span>
<span data-ttu-id="29ec7-112">如果您想要 overrite 資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="29ec7-112">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="29ec7-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="29ec7-113">-Name</span></span>
<span data-ttu-id="29ec7-114">路由篩選規則的名稱</span><span class="sxs-lookup"><span data-stu-id="29ec7-114">The name of the route filter rule</span></span>

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

### <span data-ttu-id="29ec7-115">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="29ec7-115">-RouteFilter</span></span>
<span data-ttu-id="29ec7-116">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="29ec7-116">The RouteFilter</span></span>

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

### <span data-ttu-id="29ec7-117">-確認</span><span class="sxs-lookup"><span data-stu-id="29ec7-117">-Confirm</span></span>
<span data-ttu-id="29ec7-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="29ec7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29ec7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29ec7-119">-WhatIf</span></span>
<span data-ttu-id="29ec7-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="29ec7-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29ec7-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="29ec7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29ec7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29ec7-122">-DefaultProfile</span></span>
<span data-ttu-id="29ec7-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="29ec7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29ec7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29ec7-124">CommonParameters</span></span>
<span data-ttu-id="29ec7-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="29ec7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29ec7-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="29ec7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29ec7-127">輸入</span><span class="sxs-lookup"><span data-stu-id="29ec7-127">INPUTS</span></span>

### <span data-ttu-id="29ec7-128">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="29ec7-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="29ec7-129">輸出</span><span class="sxs-lookup"><span data-stu-id="29ec7-129">OUTPUTS</span></span>

### <span data-ttu-id="29ec7-130">PSRouteFilterRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="29ec7-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="29ec7-131">筆記</span><span class="sxs-lookup"><span data-stu-id="29ec7-131">NOTES</span></span>

## <span data-ttu-id="29ec7-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="29ec7-132">RELATED LINKS</span></span>

