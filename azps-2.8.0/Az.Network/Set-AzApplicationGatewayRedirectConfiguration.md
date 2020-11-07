---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 746d1bb37bd49acfdc0a353c9985508f50514073
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789018"
---
# <span data-ttu-id="6237e-101">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6237e-101">Set-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="6237e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6237e-102">SYNOPSIS</span></span>
<span data-ttu-id="6237e-103">在現有的應用程式閘道上設定重新導向配置。</span><span class="sxs-lookup"><span data-stu-id="6237e-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="6237e-104">句法</span><span class="sxs-lookup"><span data-stu-id="6237e-104">SYNTAX</span></span>

### <span data-ttu-id="6237e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6237e-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6237e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6237e-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6237e-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="6237e-107">SetByURL</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6237e-108">說明</span><span class="sxs-lookup"><span data-stu-id="6237e-108">DESCRIPTION</span></span>
<span data-ttu-id="6237e-109">**AzApplicationGatewayRequestRoutingRule** Cmdlet 會修改重新導向設定。</span><span class="sxs-lookup"><span data-stu-id="6237e-109">**The Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="6237e-110">示例</span><span class="sxs-lookup"><span data-stu-id="6237e-110">EXAMPLES</span></span>

### <span data-ttu-id="6237e-111">範例1</span><span class="sxs-lookup"><span data-stu-id="6237e-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="6237e-112">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="6237e-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6237e-113">第二個命令會修改應用程式閘道的重新導向設定，以重新導向類型永久，並使用目標 url。</span><span class="sxs-lookup"><span data-stu-id="6237e-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="6237e-114">參數</span><span class="sxs-lookup"><span data-stu-id="6237e-114">PARAMETERS</span></span>

### <span data-ttu-id="6237e-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6237e-115">-ApplicationGateway</span></span>
<span data-ttu-id="6237e-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6237e-116">The applicationGateway</span></span>

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

### <span data-ttu-id="6237e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6237e-117">-DefaultProfile</span></span>
<span data-ttu-id="6237e-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6237e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6237e-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="6237e-119">-IncludePath</span></span>
<span data-ttu-id="6237e-120">在重新導向的 url 中包含路徑。</span><span class="sxs-lookup"><span data-stu-id="6237e-120">Include path in the redirected url.</span></span>
<span data-ttu-id="6237e-121">預設值為 true。</span><span class="sxs-lookup"><span data-stu-id="6237e-121">Default is true.</span></span>

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

### <span data-ttu-id="6237e-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="6237e-122">-IncludeQueryString</span></span>
<span data-ttu-id="6237e-123">在重新導向的 url 中包含查詢字串。</span><span class="sxs-lookup"><span data-stu-id="6237e-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="6237e-124">預設值為 true。</span><span class="sxs-lookup"><span data-stu-id="6237e-124">Default is true.</span></span>

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

### <span data-ttu-id="6237e-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="6237e-125">-Name</span></span>
<span data-ttu-id="6237e-126">重新導向配置的名稱</span><span class="sxs-lookup"><span data-stu-id="6237e-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="6237e-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="6237e-127">-RedirectType</span></span>
<span data-ttu-id="6237e-128">重新導向的類型</span><span class="sxs-lookup"><span data-stu-id="6237e-128">The type of redirect</span></span>

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

### <span data-ttu-id="6237e-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="6237e-129">-TargetListener</span></span>
<span data-ttu-id="6237e-130">[HTTP 偵聽程式] 可將要求重新導向至</span><span class="sxs-lookup"><span data-stu-id="6237e-130">HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="6237e-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="6237e-131">-TargetListenerID</span></span>
<span data-ttu-id="6237e-132">要將要求重新導向至的 HTTP 偵聽程式識別碼</span><span class="sxs-lookup"><span data-stu-id="6237e-132">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="6237e-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="6237e-133">-TargetUrl</span></span>
<span data-ttu-id="6237e-134">目標 URL fo</span><span class="sxs-lookup"><span data-stu-id="6237e-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="6237e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6237e-135">CommonParameters</span></span>
<span data-ttu-id="6237e-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6237e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6237e-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6237e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6237e-138">輸入</span><span class="sxs-lookup"><span data-stu-id="6237e-138">INPUTS</span></span>

### <span data-ttu-id="6237e-139">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6237e-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6237e-140">輸出</span><span class="sxs-lookup"><span data-stu-id="6237e-140">OUTPUTS</span></span>

### <span data-ttu-id="6237e-141">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6237e-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6237e-142">筆記</span><span class="sxs-lookup"><span data-stu-id="6237e-142">NOTES</span></span>

## <span data-ttu-id="6237e-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="6237e-143">RELATED LINKS</span></span>

[<span data-ttu-id="6237e-144">附加 AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6237e-144">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="6237e-145">AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6237e-145">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="6237e-146">新-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6237e-146">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="6237e-147">移除-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6237e-147">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)
