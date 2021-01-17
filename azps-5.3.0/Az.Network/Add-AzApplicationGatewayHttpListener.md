---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: f769eb91d524bc9115199127833471246f6fdd1f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98287247"
---
# <span data-ttu-id="7342c-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7342c-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="7342c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7342c-102">SYNOPSIS</span></span>
<span data-ttu-id="7342c-103">將 HTTP 偵聽程式新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="7342c-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="7342c-104">句法</span><span class="sxs-lookup"><span data-stu-id="7342c-104">SYNTAX</span></span>

### <span data-ttu-id="7342c-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7342c-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-SslProfileId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7342c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7342c-106">SetByResource</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-SslProfile <PSApplicationGatewaySslProfile>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7342c-107">說明</span><span class="sxs-lookup"><span data-stu-id="7342c-107">DESCRIPTION</span></span>
<span data-ttu-id="7342c-108">**AzApplicationGatewayHttpListener** Cmdlet 會將 HTTP 偵聽程式新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="7342c-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="7342c-109">示例</span><span class="sxs-lookup"><span data-stu-id="7342c-109">EXAMPLES</span></span>

### <span data-ttu-id="7342c-110">範例1：新增 HTTP 偵聽程式</span><span class="sxs-lookup"><span data-stu-id="7342c-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="7342c-111">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會將 HTTP 監聽器新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="7342c-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="7342c-112">範例2：新增具有 SSL 的 HTTPS 偵聽程式</span><span class="sxs-lookup"><span data-stu-id="7342c-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="7342c-113">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="7342c-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7342c-114">第二個命令會將使用 HTTPS 通訊協定的監聽器新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="7342c-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

### <span data-ttu-id="7342c-115">範例3：新增具有 SSL 和主機名稱的 HTTPS 偵聽程式</span><span class="sxs-lookup"><span data-stu-id="7342c-115">Example 3: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com","www.microsoft.com"
```

<span data-ttu-id="7342c-116">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="7342c-116">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7342c-117">第二個命令會將偵聽程式（使用 HTTPS 通訊協定，以及 SSL 憑證和主機名稱）新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="7342c-117">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="7342c-118">參數</span><span class="sxs-lookup"><span data-stu-id="7342c-118">PARAMETERS</span></span>

### <span data-ttu-id="7342c-119">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7342c-119">-ApplicationGateway</span></span>
<span data-ttu-id="7342c-120">指定此 Cmdlet 新增 HTTP 偵聽程式的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="7342c-120">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="7342c-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="7342c-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="7342c-122">應用程式閘道的客戶錯誤</span><span class="sxs-lookup"><span data-stu-id="7342c-122">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7342c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7342c-123">-DefaultProfile</span></span>
<span data-ttu-id="7342c-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7342c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7342c-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="7342c-125">-FirewallPolicy</span></span>
<span data-ttu-id="7342c-126">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="7342c-126">FirewallPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7342c-127">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="7342c-127">-FirewallPolicyId</span></span>
<span data-ttu-id="7342c-128">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="7342c-128">FirewallPolicyId</span></span>

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

### <span data-ttu-id="7342c-129">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7342c-129">-FrontendIPConfiguration</span></span>
<span data-ttu-id="7342c-130">指定應用程式閘道前端 IP 資源物件。</span><span class="sxs-lookup"><span data-stu-id="7342c-130">Specifies the application gateway front-end IP resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7342c-131">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7342c-131">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="7342c-132">指定應用程式閘道前端 IP ID。</span><span class="sxs-lookup"><span data-stu-id="7342c-132">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="7342c-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="7342c-133">-FrontendPort</span></span>
<span data-ttu-id="7342c-134">指定應用程式閘道的 [前端埠] 物件。</span><span class="sxs-lookup"><span data-stu-id="7342c-134">Specifies the application gateway front-end port object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7342c-135">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="7342c-135">-FrontendPortId</span></span>
<span data-ttu-id="7342c-136">指定應用程式閘道前端埠 ID。</span><span class="sxs-lookup"><span data-stu-id="7342c-136">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="7342c-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="7342c-137">-HostName</span></span>
<span data-ttu-id="7342c-138">指定此 Cmdlet 新增 HTTP 偵聽程式的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="7342c-138">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="7342c-139">-主機名稱</span><span class="sxs-lookup"><span data-stu-id="7342c-139">-HostNames</span></span>
<span data-ttu-id="7342c-140">主機名稱</span><span class="sxs-lookup"><span data-stu-id="7342c-140">Host names</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7342c-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="7342c-141">-Name</span></span>
<span data-ttu-id="7342c-142">指定此命令所新增之前端埠的名稱。</span><span class="sxs-lookup"><span data-stu-id="7342c-142">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="7342c-143">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="7342c-143">-Protocol</span></span>
<span data-ttu-id="7342c-144">指定 HTTP 偵聽程式的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="7342c-144">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="7342c-145">支援 HTTP 和 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="7342c-145">Both HTTP and HTTPS are supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7342c-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="7342c-146">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7342c-147">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="7342c-147">-SslCertificate</span></span>
<span data-ttu-id="7342c-148">指定 HTTP 偵聽程式的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="7342c-148">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="7342c-149">如果將 HTTPS 選作偵聽程式通訊協定，則必須指定。</span><span class="sxs-lookup"><span data-stu-id="7342c-149">Must be specified if HTTPS is chosen as listener protocol.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7342c-150">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="7342c-150">-SslCertificateId</span></span>
<span data-ttu-id="7342c-151">指定 HTTP 偵聽程式的 SSL 憑證 ID。</span><span class="sxs-lookup"><span data-stu-id="7342c-151">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="7342c-152">如果將 HTTPS 選作偵聽程式通訊協定，則必須指定。</span><span class="sxs-lookup"><span data-stu-id="7342c-152">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="7342c-153">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="7342c-153">-SslProfile</span></span>
<span data-ttu-id="7342c-154">SslProfile</span><span class="sxs-lookup"><span data-stu-id="7342c-154">SslProfile</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7342c-155">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="7342c-155">-SslProfileId</span></span>
<span data-ttu-id="7342c-156">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="7342c-156">SslProfileId</span></span>

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

### <span data-ttu-id="7342c-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7342c-157">CommonParameters</span></span>
<span data-ttu-id="7342c-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7342c-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7342c-159">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7342c-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7342c-160">輸入</span><span class="sxs-lookup"><span data-stu-id="7342c-160">INPUTS</span></span>

### <span data-ttu-id="7342c-161">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7342c-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7342c-162">輸出</span><span class="sxs-lookup"><span data-stu-id="7342c-162">OUTPUTS</span></span>

### <span data-ttu-id="7342c-163">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7342c-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7342c-164">筆記</span><span class="sxs-lookup"><span data-stu-id="7342c-164">NOTES</span></span>

## <span data-ttu-id="7342c-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="7342c-165">RELATED LINKS</span></span>

[<span data-ttu-id="7342c-166">AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7342c-166">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="7342c-167">新-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7342c-167">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="7342c-168">移除-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7342c-168">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="7342c-169">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7342c-169">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


