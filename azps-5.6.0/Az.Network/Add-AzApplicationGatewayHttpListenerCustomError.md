---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: d7ca75fbd2d033f35fa237113bc32bdc4699955a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909578"
---
# <span data-ttu-id="a523b-101">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="a523b-101">Add-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="a523b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a523b-102">SYNOPSIS</span></span>
<span data-ttu-id="a523b-103">新增自訂錯誤至應用程式閘道的 HTTP 聆聽者。</span><span class="sxs-lookup"><span data-stu-id="a523b-103">Adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="a523b-104">語法</span><span class="sxs-lookup"><span data-stu-id="a523b-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a523b-105">描述</span><span class="sxs-lookup"><span data-stu-id="a523b-105">DESCRIPTION</span></span>
<span data-ttu-id="a523b-106">**Add-AzApplicationGatewayCustomError** Cmdlet 會將自訂錯誤新增到應用程式閘道的 HTTP 聆聽者。</span><span class="sxs-lookup"><span data-stu-id="a523b-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="a523b-107">例子</span><span class="sxs-lookup"><span data-stu-id="a523b-107">EXAMPLES</span></span>

### <span data-ttu-id="a523b-108">範例 1：新增自訂錯誤至 HTTP 聆聽者層級</span><span class="sxs-lookup"><span data-stu-id="a523b-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="a523b-109">此命令會將 HTTP 狀態碼 502 的自訂錯誤新$listener 01，並返回更新的聆聽者。</span><span class="sxs-lookup"><span data-stu-id="a523b-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="a523b-110">參數</span><span class="sxs-lookup"><span data-stu-id="a523b-110">PARAMETERS</span></span>

### <span data-ttu-id="a523b-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="a523b-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="a523b-112">應用程式閘道客戶錯誤的錯誤頁面 URL。</span><span class="sxs-lookup"><span data-stu-id="a523b-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="a523b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a523b-113">-DefaultProfile</span></span>
<span data-ttu-id="a523b-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a523b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a523b-115">-HTTPListener</span><span class="sxs-lookup"><span data-stu-id="a523b-115">-HttpListener</span></span>
<span data-ttu-id="a523b-116">應用程式閘道 HTTP Listener</span><span class="sxs-lookup"><span data-stu-id="a523b-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="a523b-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="a523b-117">-StatusCode</span></span>
<span data-ttu-id="a523b-118">應用程式閘道客戶錯誤的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="a523b-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="a523b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a523b-119">CommonParameters</span></span>
<span data-ttu-id="a523b-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a523b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a523b-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a523b-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a523b-122">輸入</span><span class="sxs-lookup"><span data-stu-id="a523b-122">INPUTS</span></span>

### <span data-ttu-id="a523b-123">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a523b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="a523b-124">輸出</span><span class="sxs-lookup"><span data-stu-id="a523b-124">OUTPUTS</span></span>

### <span data-ttu-id="a523b-125">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="a523b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="a523b-126">筆記</span><span class="sxs-lookup"><span data-stu-id="a523b-126">NOTES</span></span>

## <span data-ttu-id="a523b-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="a523b-127">RELATED LINKS</span></span>

[<span data-ttu-id="a523b-128">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="a523b-128">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="a523b-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="a523b-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="a523b-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="a523b-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
