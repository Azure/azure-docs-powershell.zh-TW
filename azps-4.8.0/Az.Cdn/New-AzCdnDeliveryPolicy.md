---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
ms.openlocfilehash: a00e8d11868ae487357f1105d2bc2ae3934a9db9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127717"
---
# <span data-ttu-id="1f179-101">New-AzCdnDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="1f179-101">New-AzCdnDeliveryPolicy</span></span>

## <span data-ttu-id="1f179-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1f179-102">SYNOPSIS</span></span>
<span data-ttu-id="1f179-103">建立傳遞原則。</span><span class="sxs-lookup"><span data-stu-id="1f179-103">Creates a delivery policy.</span></span>

## <span data-ttu-id="1f179-104">句法</span><span class="sxs-lookup"><span data-stu-id="1f179-104">SYNTAX</span></span>

```
New-AzCdnDeliveryPolicy [-Description <String>] -Rule <PSDeliveryRule[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f179-105">說明</span><span class="sxs-lookup"><span data-stu-id="1f179-105">DESCRIPTION</span></span>
<span data-ttu-id="1f179-106">**新的-AzCdnDeliveryPolicy** Cmdlet 會建立 CDN 端點建立的傳遞原則。</span><span class="sxs-lookup"><span data-stu-id="1f179-106">The **New-AzCdnDeliveryPolicy** cmdlet creates a delivery policy for CDN endpoint creation.</span></span>

## <span data-ttu-id="1f179-107">示例</span><span class="sxs-lookup"><span data-stu-id="1f179-107">EXAMPLES</span></span>

### <span data-ttu-id="1f179-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1f179-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryPolicy -Description "Sample Policy" -Rule $rule

Description   Rules
-----------   -----
Sample Policy {rule1}
```

<span data-ttu-id="1f179-109">建立範例傳遞原則</span><span class="sxs-lookup"><span data-stu-id="1f179-109">Create a sample delivery policy</span></span>

## <span data-ttu-id="1f179-110">參數</span><span class="sxs-lookup"><span data-stu-id="1f179-110">PARAMETERS</span></span>

### <span data-ttu-id="1f179-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f179-111">-DefaultProfile</span></span>
<span data-ttu-id="1f179-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f179-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f179-113">-描述</span><span class="sxs-lookup"><span data-stu-id="1f179-113">-Description</span></span>
<span data-ttu-id="1f179-114">原則描述</span><span class="sxs-lookup"><span data-stu-id="1f179-114">Description of the policy</span></span>

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

### <span data-ttu-id="1f179-115">-規則</span><span class="sxs-lookup"><span data-stu-id="1f179-115">-Rule</span></span>
<span data-ttu-id="1f179-116">DeliveryRules 清單。</span><span class="sxs-lookup"><span data-stu-id="1f179-116">A list of deliveryRules.</span></span>

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

### <span data-ttu-id="1f179-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f179-117">CommonParameters</span></span>
<span data-ttu-id="1f179-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1f179-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f179-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1f179-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f179-120">輸入</span><span class="sxs-lookup"><span data-stu-id="1f179-120">INPUTS</span></span>

### <span data-ttu-id="1f179-121">所有</span><span class="sxs-lookup"><span data-stu-id="1f179-121">None</span></span>

## <span data-ttu-id="1f179-122">輸出</span><span class="sxs-lookup"><span data-stu-id="1f179-122">OUTPUTS</span></span>

### <span data-ttu-id="1f179-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="1f179-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span></span>

## <span data-ttu-id="1f179-124">筆記</span><span class="sxs-lookup"><span data-stu-id="1f179-124">NOTES</span></span>

## <span data-ttu-id="1f179-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f179-125">RELATED LINKS</span></span>