---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: f3b641e3e9229706f3010e7db95480423b06361c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800429"
---
# <span data-ttu-id="bb184-101">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bb184-101">Get-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="bb184-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bb184-102">SYNOPSIS</span></span>
<span data-ttu-id="bb184-103">{{填入摘要}}</span><span class="sxs-lookup"><span data-stu-id="bb184-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb184-104">句法</span><span class="sxs-lookup"><span data-stu-id="bb184-104">SYNTAX</span></span>

```
Get-AzureRmRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb184-105">說明</span><span class="sxs-lookup"><span data-stu-id="bb184-105">DESCRIPTION</span></span>
<span data-ttu-id="bb184-106">{{填入描述}}</span><span class="sxs-lookup"><span data-stu-id="bb184-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="bb184-107">示例</span><span class="sxs-lookup"><span data-stu-id="bb184-107">EXAMPLES</span></span>

### <span data-ttu-id="bb184-108">範例1</span><span class="sxs-lookup"><span data-stu-id="bb184-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="bb184-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="bb184-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="bb184-110">參數</span><span class="sxs-lookup"><span data-stu-id="bb184-110">PARAMETERS</span></span>

### <span data-ttu-id="bb184-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb184-111">-DefaultProfile</span></span>
<span data-ttu-id="bb184-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bb184-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb184-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="bb184-113">-Name</span></span>
<span data-ttu-id="bb184-114">路由篩選規則的名稱</span><span class="sxs-lookup"><span data-stu-id="bb184-114">The name of the route filter rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb184-115">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="bb184-115">-RouteFilter</span></span>
<span data-ttu-id="bb184-116">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="bb184-116">The RouteFilter</span></span>

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

### <span data-ttu-id="bb184-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb184-117">CommonParameters</span></span>
<span data-ttu-id="bb184-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bb184-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb184-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bb184-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb184-120">輸入</span><span class="sxs-lookup"><span data-stu-id="bb184-120">INPUTS</span></span>

### <span data-ttu-id="bb184-121">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bb184-121">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="bb184-122">輸出</span><span class="sxs-lookup"><span data-stu-id="bb184-122">OUTPUTS</span></span>

### <span data-ttu-id="bb184-123">PSRouteFilterRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bb184-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="bb184-124">筆記</span><span class="sxs-lookup"><span data-stu-id="bb184-124">NOTES</span></span>

## <span data-ttu-id="bb184-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb184-125">RELATED LINKS</span></span>

