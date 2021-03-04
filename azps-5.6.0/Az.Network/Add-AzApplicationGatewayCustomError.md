---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
ms.openlocfilehash: f5c36cc9e6133fbde4e7bae34b4bc6b479afb96e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905921"
---
# <span data-ttu-id="63393-101">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="63393-101">Add-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="63393-102">簡介</span><span class="sxs-lookup"><span data-stu-id="63393-102">SYNOPSIS</span></span>
<span data-ttu-id="63393-103">新增自訂錯誤至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="63393-103">Adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="63393-104">語法</span><span class="sxs-lookup"><span data-stu-id="63393-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63393-105">描述</span><span class="sxs-lookup"><span data-stu-id="63393-105">DESCRIPTION</span></span>
<span data-ttu-id="63393-106">**Add-AzApplicationGatewayCustomError** Cmdlet 會新增自訂錯誤至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="63393-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="63393-107">例子</span><span class="sxs-lookup"><span data-stu-id="63393-107">EXAMPLES</span></span>

### <span data-ttu-id="63393-108">範例 1：新增自訂錯誤至應用程式閘道層級</span><span class="sxs-lookup"><span data-stu-id="63393-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $resourceGroupName = "resourceGroupName"
PS C:\> $AppGWName = "applicationGatewayName"
PS C:\> $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroup $resourceGroupName
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzApplicationGatewayCustomError -ApplicationGateway $AppGw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
PS C:\> Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="63393-109">此命令會將 HTTP 狀態碼 502 的自訂錯誤新$appgw應用程式閘道，並返回更新的閘道。</span><span class="sxs-lookup"><span data-stu-id="63393-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

### <span data-ttu-id="63393-110">範例 2：新增自訂錯誤至應用程式閘道聆聽者層級</span><span class="sxs-lookup"><span data-stu-id="63393-110">Example 2: Adds custom error to application gateway listener level</span></span>
```powershell
 $resourceGroupName = "resourceGroupName"
 $AppGWName = "applicationGatewayName"
 $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
 $listenerName = "listenerName"
 $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroupName $resourceGroupName
 $listener = Get-AzApplicationGatewayHttpListener -ApplicationGateway $AppGW -Name $listenerName
 $updatedListener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url 
 Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="63393-111">此命令會將 HTTP 狀態碼 502 的自訂錯誤新$appgw至聆聽者層級的應用程式閘道，並返回更新的閘道。</span><span class="sxs-lookup"><span data-stu-id="63393-111">This command adds a custom error of http status code 502 to the application gateway $appgw at the listener level, and return the updated gateway.</span></span>

## <span data-ttu-id="63393-112">參數</span><span class="sxs-lookup"><span data-stu-id="63393-112">PARAMETERS</span></span>

### <span data-ttu-id="63393-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63393-113">-ApplicationGateway</span></span>
<span data-ttu-id="63393-114">應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="63393-114">The Application Gateway</span></span>

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

### <span data-ttu-id="63393-115">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="63393-115">-CustomErrorPageUrl</span></span>
<span data-ttu-id="63393-116">應用程式閘道客戶錯誤的錯誤頁面 URL。</span><span class="sxs-lookup"><span data-stu-id="63393-116">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="63393-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63393-117">-DefaultProfile</span></span>
<span data-ttu-id="63393-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="63393-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63393-119">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="63393-119">-StatusCode</span></span>
<span data-ttu-id="63393-120">應用程式閘道客戶錯誤的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="63393-120">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="63393-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63393-121">CommonParameters</span></span>
<span data-ttu-id="63393-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="63393-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63393-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="63393-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63393-124">輸入</span><span class="sxs-lookup"><span data-stu-id="63393-124">INPUTS</span></span>

### <span data-ttu-id="63393-125">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63393-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="63393-126">輸出</span><span class="sxs-lookup"><span data-stu-id="63393-126">OUTPUTS</span></span>

### <span data-ttu-id="63393-127">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="63393-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="63393-128">筆記</span><span class="sxs-lookup"><span data-stu-id="63393-128">NOTES</span></span>

## <span data-ttu-id="63393-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="63393-129">RELATED LINKS</span></span>

[<span data-ttu-id="63393-130">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="63393-130">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="63393-131">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="63393-131">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="63393-132">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="63393-132">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="63393-133">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="63393-133">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
