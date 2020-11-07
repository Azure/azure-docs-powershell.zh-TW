---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 96122c68317166f078d40be8cee9d0124c4d713e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624044"
---
# <span data-ttu-id="c6dee-101">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c6dee-101">Get-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="c6dee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c6dee-102">SYNOPSIS</span></span>
<span data-ttu-id="c6dee-103">{{填入摘要}}</span><span class="sxs-lookup"><span data-stu-id="c6dee-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6dee-104">句法</span><span class="sxs-lookup"><span data-stu-id="c6dee-104">SYNTAX</span></span>

```
Get-AzureRmRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6dee-105">說明</span><span class="sxs-lookup"><span data-stu-id="c6dee-105">DESCRIPTION</span></span>
<span data-ttu-id="c6dee-106">{{填入描述}}</span><span class="sxs-lookup"><span data-stu-id="c6dee-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="c6dee-107">示例</span><span class="sxs-lookup"><span data-stu-id="c6dee-107">EXAMPLES</span></span>

### <span data-ttu-id="c6dee-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c6dee-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="c6dee-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="c6dee-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="c6dee-110">參數</span><span class="sxs-lookup"><span data-stu-id="c6dee-110">PARAMETERS</span></span>

### <span data-ttu-id="c6dee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6dee-111">-DefaultProfile</span></span>
<span data-ttu-id="c6dee-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6dee-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6dee-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="c6dee-113">-Name</span></span>
<span data-ttu-id="c6dee-114">路由篩選規則的名稱</span><span class="sxs-lookup"><span data-stu-id="c6dee-114">The name of the route filter rule</span></span>

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

### <span data-ttu-id="c6dee-115">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="c6dee-115">-RouteFilter</span></span>
<span data-ttu-id="c6dee-116">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="c6dee-116">The RouteFilter</span></span>

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

### <span data-ttu-id="c6dee-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6dee-117">CommonParameters</span></span>
<span data-ttu-id="c6dee-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c6dee-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6dee-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c6dee-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6dee-120">輸入</span><span class="sxs-lookup"><span data-stu-id="c6dee-120">INPUTS</span></span>

### <span data-ttu-id="c6dee-121">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c6dee-121">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>
<span data-ttu-id="c6dee-122">參數： RouteFilter (ByValue) </span><span class="sxs-lookup"><span data-stu-id="c6dee-122">Parameters: RouteFilter (ByValue)</span></span>

## <span data-ttu-id="c6dee-123">輸出</span><span class="sxs-lookup"><span data-stu-id="c6dee-123">OUTPUTS</span></span>

### <span data-ttu-id="c6dee-124">PSRouteFilterRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c6dee-124">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="c6dee-125">筆記</span><span class="sxs-lookup"><span data-stu-id="c6dee-125">NOTES</span></span>

## <span data-ttu-id="c6dee-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6dee-126">RELATED LINKS</span></span>
