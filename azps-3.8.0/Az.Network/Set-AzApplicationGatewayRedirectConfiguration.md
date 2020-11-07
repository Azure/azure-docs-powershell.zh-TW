---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: da6acfddcee30861b73145d7d8e66871de02568d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957290"
---
# <span data-ttu-id="505f3-101">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="505f3-101">Set-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="505f3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="505f3-102">SYNOPSIS</span></span>
<span data-ttu-id="505f3-103">在現有的應用程式閘道上設定重新導向配置。</span><span class="sxs-lookup"><span data-stu-id="505f3-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="505f3-104">句法</span><span class="sxs-lookup"><span data-stu-id="505f3-104">SYNTAX</span></span>

### <span data-ttu-id="505f3-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="505f3-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="505f3-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="505f3-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="505f3-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="505f3-107">SetByURL</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="505f3-108">說明</span><span class="sxs-lookup"><span data-stu-id="505f3-108">DESCRIPTION</span></span>
<span data-ttu-id="505f3-109">**AzApplicationGatewayRequestRoutingRule** Cmdlet 會修改重新導向設定。</span><span class="sxs-lookup"><span data-stu-id="505f3-109">**The Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="505f3-110">示例</span><span class="sxs-lookup"><span data-stu-id="505f3-110">EXAMPLES</span></span>

### <span data-ttu-id="505f3-111">範例1</span><span class="sxs-lookup"><span data-stu-id="505f3-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="505f3-112">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="505f3-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="505f3-113">第二個命令會修改應用程式閘道的重新導向設定，以重新導向類型永久，並使用目標 url。</span><span class="sxs-lookup"><span data-stu-id="505f3-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="505f3-114">參數</span><span class="sxs-lookup"><span data-stu-id="505f3-114">PARAMETERS</span></span>

### <span data-ttu-id="505f3-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="505f3-115">-ApplicationGateway</span></span>
<span data-ttu-id="505f3-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="505f3-116">The applicationGateway</span></span>

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

### <span data-ttu-id="505f3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="505f3-117">-DefaultProfile</span></span>
<span data-ttu-id="505f3-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="505f3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="505f3-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="505f3-119">-IncludePath</span></span>
<span data-ttu-id="505f3-120">在重新導向的 url 中包含路徑。</span><span class="sxs-lookup"><span data-stu-id="505f3-120">Include path in the redirected url.</span></span>
<span data-ttu-id="505f3-121">預設值為 true。</span><span class="sxs-lookup"><span data-stu-id="505f3-121">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="505f3-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="505f3-122">-IncludeQueryString</span></span>
<span data-ttu-id="505f3-123">在重新導向的 url 中包含查詢字串。</span><span class="sxs-lookup"><span data-stu-id="505f3-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="505f3-124">預設值為 true。</span><span class="sxs-lookup"><span data-stu-id="505f3-124">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="505f3-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="505f3-125">-Name</span></span>
<span data-ttu-id="505f3-126">重新導向配置的名稱</span><span class="sxs-lookup"><span data-stu-id="505f3-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="505f3-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="505f3-127">-RedirectType</span></span>
<span data-ttu-id="505f3-128">重新導向的類型</span><span class="sxs-lookup"><span data-stu-id="505f3-128">The type of redirect</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="505f3-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="505f3-129">-TargetListener</span></span>
<span data-ttu-id="505f3-130">[HTTP 偵聽程式] 可將要求重新導向至</span><span class="sxs-lookup"><span data-stu-id="505f3-130">HTTP listener to redirect the request to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="505f3-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="505f3-131">-TargetListenerID</span></span>
<span data-ttu-id="505f3-132">要將要求重新導向至的 HTTP 偵聽程式識別碼</span><span class="sxs-lookup"><span data-stu-id="505f3-132">ID of HTTP listener to redirect the request to</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="505f3-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="505f3-133">-TargetUrl</span></span>
<span data-ttu-id="505f3-134">目標 URL fo</span><span class="sxs-lookup"><span data-stu-id="505f3-134">Target URL fo redirection</span></span>

```yaml
Type: System.String
Parameter Sets: SetByURL
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="505f3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="505f3-135">CommonParameters</span></span>
<span data-ttu-id="505f3-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="505f3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="505f3-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="505f3-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="505f3-138">輸入</span><span class="sxs-lookup"><span data-stu-id="505f3-138">INPUTS</span></span>

### <span data-ttu-id="505f3-139">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="505f3-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="505f3-140">輸出</span><span class="sxs-lookup"><span data-stu-id="505f3-140">OUTPUTS</span></span>

### <span data-ttu-id="505f3-141">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="505f3-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="505f3-142">筆記</span><span class="sxs-lookup"><span data-stu-id="505f3-142">NOTES</span></span>

## <span data-ttu-id="505f3-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="505f3-143">RELATED LINKS</span></span>

[<span data-ttu-id="505f3-144">附加 AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="505f3-144">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="505f3-145">AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="505f3-145">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="505f3-146">新-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="505f3-146">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="505f3-147">移除-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="505f3-147">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)
