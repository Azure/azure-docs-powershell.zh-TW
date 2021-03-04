---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 990c9624d949fa695b815a9530125a90693816ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901962"
---
# <span data-ttu-id="37f9b-101">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="37f9b-101">Remove-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="37f9b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="37f9b-102">SYNOPSIS</span></span>
<span data-ttu-id="37f9b-103">從應用程式閘道移除自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="37f9b-103">Removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="37f9b-104">語法</span><span class="sxs-lookup"><span data-stu-id="37f9b-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37f9b-105">描述</span><span class="sxs-lookup"><span data-stu-id="37f9b-105">DESCRIPTION</span></span>
<span data-ttu-id="37f9b-106">**Remove-AzApplicationGatewayCustomError** Cmdlet 會從應用程式閘道移除自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="37f9b-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="37f9b-107">例子</span><span class="sxs-lookup"><span data-stu-id="37f9b-107">EXAMPLES</span></span>

### <span data-ttu-id="37f9b-108">範例 1：移除應用程式閘道的自訂錯誤</span><span class="sxs-lookup"><span data-stu-id="37f9b-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="37f9b-109">此命令會從應用程式閘道移除 HTTP 狀態碼 502 的自訂錯誤$appgw，並返回更新的閘道。</span><span class="sxs-lookup"><span data-stu-id="37f9b-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="37f9b-110">參數</span><span class="sxs-lookup"><span data-stu-id="37f9b-110">PARAMETERS</span></span>

### <span data-ttu-id="37f9b-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37f9b-111">-ApplicationGateway</span></span>
<span data-ttu-id="37f9b-112">應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="37f9b-112">The Application Gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37f9b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37f9b-113">-DefaultProfile</span></span>
<span data-ttu-id="37f9b-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="37f9b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37f9b-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="37f9b-115">-StatusCode</span></span>
<span data-ttu-id="37f9b-116">應用程式閘道客戶錯誤的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="37f9b-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="37f9b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37f9b-117">CommonParameters</span></span>
<span data-ttu-id="37f9b-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="37f9b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37f9b-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="37f9b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37f9b-120">輸入</span><span class="sxs-lookup"><span data-stu-id="37f9b-120">INPUTS</span></span>

### <span data-ttu-id="37f9b-121">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37f9b-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="37f9b-122">輸出</span><span class="sxs-lookup"><span data-stu-id="37f9b-122">OUTPUTS</span></span>

### <span data-ttu-id="37f9b-123">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="37f9b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="37f9b-124">筆記</span><span class="sxs-lookup"><span data-stu-id="37f9b-124">NOTES</span></span>

## <span data-ttu-id="37f9b-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="37f9b-125">RELATED LINKS</span></span>

[<span data-ttu-id="37f9b-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="37f9b-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="37f9b-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="37f9b-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="37f9b-128">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="37f9b-128">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="37f9b-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="37f9b-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
