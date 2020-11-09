---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 91de215282dc05be2136237fa5fb2b244d7f0c4a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94288260"
---
# <span data-ttu-id="58ed3-101">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="58ed3-101">Remove-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="58ed3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58ed3-102">SYNOPSIS</span></span>
<span data-ttu-id="58ed3-103">從應用程式閘道移除自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="58ed3-103">Removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="58ed3-104">句法</span><span class="sxs-lookup"><span data-stu-id="58ed3-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58ed3-105">說明</span><span class="sxs-lookup"><span data-stu-id="58ed3-105">DESCRIPTION</span></span>
<span data-ttu-id="58ed3-106">**AzApplicationGatewayCustomError** Cmdlet 會從應用程式閘道中移除自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="58ed3-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="58ed3-107">示例</span><span class="sxs-lookup"><span data-stu-id="58ed3-107">EXAMPLES</span></span>

### <span data-ttu-id="58ed3-108">範例1：從應用程式閘道移除自訂錯誤</span><span class="sxs-lookup"><span data-stu-id="58ed3-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="58ed3-109">這個命令會從應用程式閘道 $appgw 中移除 HTTP 狀態碼502的自訂錯誤，並傳回更新的閘道。</span><span class="sxs-lookup"><span data-stu-id="58ed3-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="58ed3-110">參數</span><span class="sxs-lookup"><span data-stu-id="58ed3-110">PARAMETERS</span></span>

### <span data-ttu-id="58ed3-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="58ed3-111">-ApplicationGateway</span></span>
<span data-ttu-id="58ed3-112">應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="58ed3-112">The Application Gateway</span></span>

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

### <span data-ttu-id="58ed3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58ed3-113">-DefaultProfile</span></span>
<span data-ttu-id="58ed3-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="58ed3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58ed3-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="58ed3-115">-StatusCode</span></span>
<span data-ttu-id="58ed3-116">應用程式閘道客戶錯誤的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="58ed3-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="58ed3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58ed3-117">CommonParameters</span></span>
<span data-ttu-id="58ed3-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58ed3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58ed3-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="58ed3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58ed3-120">輸入</span><span class="sxs-lookup"><span data-stu-id="58ed3-120">INPUTS</span></span>

### <span data-ttu-id="58ed3-121">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="58ed3-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="58ed3-122">輸出</span><span class="sxs-lookup"><span data-stu-id="58ed3-122">OUTPUTS</span></span>

### <span data-ttu-id="58ed3-123">PSApplicationGatewayCustomError 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="58ed3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="58ed3-124">筆記</span><span class="sxs-lookup"><span data-stu-id="58ed3-124">NOTES</span></span>

## <span data-ttu-id="58ed3-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="58ed3-125">RELATED LINKS</span></span>

[<span data-ttu-id="58ed3-126">附加 AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="58ed3-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="58ed3-127">AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="58ed3-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="58ed3-128">新-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="58ed3-128">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="58ed3-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="58ed3-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
