---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: fabe88c2b7606bac3d5a90011913a2beae513f09
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910409"
---
# <span data-ttu-id="dddf3-101">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="dddf3-101">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="dddf3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dddf3-102">SYNOPSIS</span></span>
<span data-ttu-id="dddf3-103">從應用程式閘道的 HTTP 聆聽者移除自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="dddf3-103">Removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="dddf3-104">語法</span><span class="sxs-lookup"><span data-stu-id="dddf3-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dddf3-105">描述</span><span class="sxs-lookup"><span data-stu-id="dddf3-105">DESCRIPTION</span></span>
<span data-ttu-id="dddf3-106">**Remove-AzApplicationGatewayCustomError** Cmdlet 會從應用程式閘道的 HTTP 聆聽者移除自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="dddf3-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="dddf3-107">例子</span><span class="sxs-lookup"><span data-stu-id="dddf3-107">EXAMPLES</span></span>

### <span data-ttu-id="dddf3-108">範例 1：移除 HTTP 聆聽者中的自訂錯誤</span><span class="sxs-lookup"><span data-stu-id="dddf3-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="dddf3-109">此命令會從 HTTP 聆聽程式 $listener 01 移除 HTTP 狀態碼 502 的自訂錯誤，並返回更新的聆聽者。</span><span class="sxs-lookup"><span data-stu-id="dddf3-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="dddf3-110">參數</span><span class="sxs-lookup"><span data-stu-id="dddf3-110">PARAMETERS</span></span>

### <span data-ttu-id="dddf3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dddf3-111">-DefaultProfile</span></span>
<span data-ttu-id="dddf3-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dddf3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dddf3-113">-HTTPListener</span><span class="sxs-lookup"><span data-stu-id="dddf3-113">-HttpListener</span></span>
<span data-ttu-id="dddf3-114">應用程式閘道 HTTP Listener</span><span class="sxs-lookup"><span data-stu-id="dddf3-114">The Application Gateway Http Listener</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dddf3-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="dddf3-115">-StatusCode</span></span>
<span data-ttu-id="dddf3-116">應用程式閘道客戶錯誤的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="dddf3-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="dddf3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dddf3-117">CommonParameters</span></span>
<span data-ttu-id="dddf3-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dddf3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dddf3-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="dddf3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dddf3-120">輸入</span><span class="sxs-lookup"><span data-stu-id="dddf3-120">INPUTS</span></span>

### <span data-ttu-id="dddf3-121">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="dddf3-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="dddf3-122">輸出</span><span class="sxs-lookup"><span data-stu-id="dddf3-122">OUTPUTS</span></span>

### <span data-ttu-id="dddf3-123">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="dddf3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="dddf3-124">筆記</span><span class="sxs-lookup"><span data-stu-id="dddf3-124">NOTES</span></span>

## <span data-ttu-id="dddf3-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="dddf3-125">RELATED LINKS</span></span>

[<span data-ttu-id="dddf3-126">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="dddf3-126">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="dddf3-127">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="dddf3-127">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="dddf3-128">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="dddf3-128">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
