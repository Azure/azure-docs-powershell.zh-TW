---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 63d90b646b639d7978dfbf734256976f423a3092
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902362"
---
# <span data-ttu-id="b08c3-101">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="b08c3-101">Set-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="b08c3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b08c3-102">SYNOPSIS</span></span>
<span data-ttu-id="b08c3-103">更新應用程式閘道 HTTP 聆聽者中的自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="b08c3-103">Updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="b08c3-104">語法</span><span class="sxs-lookup"><span data-stu-id="b08c3-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b08c3-105">描述</span><span class="sxs-lookup"><span data-stu-id="b08c3-105">DESCRIPTION</span></span>
<span data-ttu-id="b08c3-106">**Set-AzApplicationGatewayCustomError** Cmdlet 會更新應用程式閘道的 HTTP 聆聽者中的自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="b08c3-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="b08c3-107">例子</span><span class="sxs-lookup"><span data-stu-id="b08c3-107">EXAMPLES</span></span>

### <span data-ttu-id="b08c3-108">範例 1：從 HTTP 聆聽者更新自訂錯誤</span><span class="sxs-lookup"><span data-stu-id="b08c3-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="b08c3-109">此命令會更新 HTTP 聆聽程式 $listener 01 中 HTTP 狀態碼 502 的自訂錯誤，並返回更新的聆聽者。</span><span class="sxs-lookup"><span data-stu-id="b08c3-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="b08c3-110">參數</span><span class="sxs-lookup"><span data-stu-id="b08c3-110">PARAMETERS</span></span>

### <span data-ttu-id="b08c3-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="b08c3-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="b08c3-112">應用程式閘道客戶錯誤的錯誤頁面 URL。</span><span class="sxs-lookup"><span data-stu-id="b08c3-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="b08c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b08c3-113">-DefaultProfile</span></span>
<span data-ttu-id="b08c3-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b08c3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b08c3-115">-HTTPListener</span><span class="sxs-lookup"><span data-stu-id="b08c3-115">-HttpListener</span></span>
<span data-ttu-id="b08c3-116">應用程式閘道 HTTP Listener</span><span class="sxs-lookup"><span data-stu-id="b08c3-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="b08c3-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="b08c3-117">-StatusCode</span></span>
<span data-ttu-id="b08c3-118">應用程式閘道客戶錯誤的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="b08c3-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="b08c3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b08c3-119">CommonParameters</span></span>
<span data-ttu-id="b08c3-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b08c3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b08c3-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b08c3-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b08c3-122">輸入</span><span class="sxs-lookup"><span data-stu-id="b08c3-122">INPUTS</span></span>

### <span data-ttu-id="b08c3-123">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b08c3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="b08c3-124">輸出</span><span class="sxs-lookup"><span data-stu-id="b08c3-124">OUTPUTS</span></span>

### <span data-ttu-id="b08c3-125">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b08c3-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="b08c3-126">筆記</span><span class="sxs-lookup"><span data-stu-id="b08c3-126">NOTES</span></span>

## <span data-ttu-id="b08c3-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="b08c3-127">RELATED LINKS</span></span>

[<span data-ttu-id="b08c3-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="b08c3-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="b08c3-129">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="b08c3-129">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="b08c3-130">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="b08c3-130">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)
