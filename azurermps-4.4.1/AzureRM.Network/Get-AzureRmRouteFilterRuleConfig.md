---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: cb8c6fcca5fb64427efc17123320d1e2a8156aa3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449982"
---
# <span data-ttu-id="66fa5-101">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="66fa5-101">Get-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="66fa5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66fa5-102">SYNOPSIS</span></span>
<span data-ttu-id="66fa5-103">{{填入摘要}}</span><span class="sxs-lookup"><span data-stu-id="66fa5-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66fa5-104">句法</span><span class="sxs-lookup"><span data-stu-id="66fa5-104">SYNTAX</span></span>

```
Get-AzureRmRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66fa5-105">說明</span><span class="sxs-lookup"><span data-stu-id="66fa5-105">DESCRIPTION</span></span>
<span data-ttu-id="66fa5-106">{{填入描述}}</span><span class="sxs-lookup"><span data-stu-id="66fa5-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="66fa5-107">示例</span><span class="sxs-lookup"><span data-stu-id="66fa5-107">EXAMPLES</span></span>

### <span data-ttu-id="66fa5-108">範例1</span><span class="sxs-lookup"><span data-stu-id="66fa5-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="66fa5-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="66fa5-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="66fa5-110">參數</span><span class="sxs-lookup"><span data-stu-id="66fa5-110">PARAMETERS</span></span>

### <span data-ttu-id="66fa5-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="66fa5-111">-Name</span></span>
<span data-ttu-id="66fa5-112">路由篩選規則的名稱</span><span class="sxs-lookup"><span data-stu-id="66fa5-112">The name of the route filter rule</span></span>

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

### <span data-ttu-id="66fa5-113">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="66fa5-113">-RouteFilter</span></span>
<span data-ttu-id="66fa5-114">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="66fa5-114">The RouteFilter</span></span>

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

### <span data-ttu-id="66fa5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66fa5-115">-DefaultProfile</span></span>
<span data-ttu-id="66fa5-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="66fa5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66fa5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66fa5-117">CommonParameters</span></span>
<span data-ttu-id="66fa5-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66fa5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66fa5-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="66fa5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66fa5-120">輸入</span><span class="sxs-lookup"><span data-stu-id="66fa5-120">INPUTS</span></span>

### <span data-ttu-id="66fa5-121">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="66fa5-121">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="66fa5-122">輸出</span><span class="sxs-lookup"><span data-stu-id="66fa5-122">OUTPUTS</span></span>

### <span data-ttu-id="66fa5-123">PSRouteFilterRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="66fa5-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="66fa5-124">筆記</span><span class="sxs-lookup"><span data-stu-id="66fa5-124">NOTES</span></span>

## <span data-ttu-id="66fa5-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="66fa5-125">RELATED LINKS</span></span>

