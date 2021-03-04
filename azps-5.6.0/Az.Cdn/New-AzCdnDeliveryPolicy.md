---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdndeliverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
ms.openlocfilehash: 01cadd267a98cab239b7a83357d308d8dd2d32bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914914"
---
# <span data-ttu-id="ddec1-101">New-AzCdnDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="ddec1-101">New-AzCdnDeliveryPolicy</span></span>

## <span data-ttu-id="ddec1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ddec1-102">SYNOPSIS</span></span>
<span data-ttu-id="ddec1-103">建立傳遞策略。</span><span class="sxs-lookup"><span data-stu-id="ddec1-103">Creates a delivery policy.</span></span>

## <span data-ttu-id="ddec1-104">語法</span><span class="sxs-lookup"><span data-stu-id="ddec1-104">SYNTAX</span></span>

```
New-AzCdnDeliveryPolicy [-Description <String>] -Rule <PSDeliveryRule[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddec1-105">描述</span><span class="sxs-lookup"><span data-stu-id="ddec1-105">DESCRIPTION</span></span>
<span data-ttu-id="ddec1-106">**New-AzCdnDeliveryPolidlet** 會建立 CDN 端點的傳遞策略。</span><span class="sxs-lookup"><span data-stu-id="ddec1-106">The **New-AzCdnDeliveryPolicy** cmdlet creates a delivery policy for CDN endpoint creation.</span></span>

## <span data-ttu-id="ddec1-107">例子</span><span class="sxs-lookup"><span data-stu-id="ddec1-107">EXAMPLES</span></span>

### <span data-ttu-id="ddec1-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="ddec1-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryPolicy -Description "Sample Policy" -Rule $rule

Description   Rules
-----------   -----
Sample Policy {rule1}
```

<span data-ttu-id="ddec1-109">建立範例傳遞政策</span><span class="sxs-lookup"><span data-stu-id="ddec1-109">Create a sample delivery policy</span></span>

## <span data-ttu-id="ddec1-110">參數</span><span class="sxs-lookup"><span data-stu-id="ddec1-110">PARAMETERS</span></span>

### <span data-ttu-id="ddec1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddec1-111">-DefaultProfile</span></span>
<span data-ttu-id="ddec1-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ddec1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddec1-113">-描述</span><span class="sxs-lookup"><span data-stu-id="ddec1-113">-Description</span></span>
<span data-ttu-id="ddec1-114">該政策的描述</span><span class="sxs-lookup"><span data-stu-id="ddec1-114">Description of the policy</span></span>

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

### <span data-ttu-id="ddec1-115">-規則</span><span class="sxs-lookup"><span data-stu-id="ddec1-115">-Rule</span></span>
<span data-ttu-id="ddec1-116">傳遞規則清單。</span><span class="sxs-lookup"><span data-stu-id="ddec1-116">A list of deliveryRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddec1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddec1-117">CommonParameters</span></span>
<span data-ttu-id="ddec1-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ddec1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddec1-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ddec1-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddec1-120">輸入</span><span class="sxs-lookup"><span data-stu-id="ddec1-120">INPUTS</span></span>

### <span data-ttu-id="ddec1-121">沒有</span><span class="sxs-lookup"><span data-stu-id="ddec1-121">None</span></span>

## <span data-ttu-id="ddec1-122">輸出</span><span class="sxs-lookup"><span data-stu-id="ddec1-122">OUTPUTS</span></span>

### <span data-ttu-id="ddec1-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSD力策略</span><span class="sxs-lookup"><span data-stu-id="ddec1-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span></span>

## <span data-ttu-id="ddec1-124">筆記</span><span class="sxs-lookup"><span data-stu-id="ddec1-124">NOTES</span></span>

## <span data-ttu-id="ddec1-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="ddec1-125">RELATED LINKS</span></span>
