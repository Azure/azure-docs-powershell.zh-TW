---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 51d85ffa9c1181b45f7ea4aa45484a814759a953
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909581"
---
# <span data-ttu-id="0a46c-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0a46c-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="0a46c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0a46c-102">SYNOPSIS</span></span>
<span data-ttu-id="0a46c-103">新增 HTTP 聆聽者至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="0a46c-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="0a46c-104">語法</span><span class="sxs-lookup"><span data-stu-id="0a46c-104">SYNTAX</span></span>

### <span data-ttu-id="0a46c-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0a46c-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-SslProfileId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0a46c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0a46c-106">SetByResource</span></span>
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

## <span data-ttu-id="0a46c-107">描述</span><span class="sxs-lookup"><span data-stu-id="0a46c-107">DESCRIPTION</span></span>
<span data-ttu-id="0a46c-108">**Add-AzApplicationGatewayHttpListener** Cmdlet 會將 HTTP 聆聽者新增到應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="0a46c-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="0a46c-109">例子</span><span class="sxs-lookup"><span data-stu-id="0a46c-109">EXAMPLES</span></span>

### <span data-ttu-id="0a46c-110">範例 1：新增 HTTP 聆聽者</span><span class="sxs-lookup"><span data-stu-id="0a46c-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="0a46c-111">第一個命令會獲得應用程式閘道，並儲存在$AppGw變數。第二個命令會將 HTTP 聆聽者新增到應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="0a46c-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="0a46c-112">範例 2：使用 SSL 新增 HTTPS 聆聽者</span><span class="sxs-lookup"><span data-stu-id="0a46c-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="0a46c-113">第一個命令會獲得應用程式閘道，並儲存在$AppGw變數。</span><span class="sxs-lookup"><span data-stu-id="0a46c-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0a46c-114">第二個命令會將使用 HTTPS 通訊協定的聆聽者新增到應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="0a46c-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

### <span data-ttu-id="0a46c-115">範例 3：使用 SSL 和 HostNames 新增 HTTPS 聆聽者</span><span class="sxs-lookup"><span data-stu-id="0a46c-115">Example 3: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com","www.microsoft.com"
```

<span data-ttu-id="0a46c-116">第一個命令會獲得應用程式閘道，並儲存在$AppGw變數。</span><span class="sxs-lookup"><span data-stu-id="0a46c-116">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0a46c-117">第二個命令會將使用 HTTPS 通訊協定與 SSL 憑證和 HostName 的聆聽者新增到應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="0a46c-117">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="0a46c-118">參數</span><span class="sxs-lookup"><span data-stu-id="0a46c-118">PARAMETERS</span></span>

### <span data-ttu-id="0a46c-119">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a46c-119">-ApplicationGateway</span></span>
<span data-ttu-id="0a46c-120">指定此 Cmdlet 新增 HTTP 聆聽者的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="0a46c-120">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="0a46c-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a46c-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="0a46c-122">應用程式閘道的客戶錯誤</span><span class="sxs-lookup"><span data-stu-id="0a46c-122">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="0a46c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a46c-123">-DefaultProfile</span></span>
<span data-ttu-id="0a46c-124">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a46c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a46c-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="0a46c-125">-FirewallPolicy</span></span>
<span data-ttu-id="0a46c-126">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="0a46c-126">FirewallPolicy</span></span>

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

### <span data-ttu-id="0a46c-127">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="0a46c-127">-FirewallPolicyId</span></span>
<span data-ttu-id="0a46c-128">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="0a46c-128">FirewallPolicyId</span></span>

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

### <span data-ttu-id="0a46c-129">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a46c-129">-FrontendIPConfiguration</span></span>
<span data-ttu-id="0a46c-130">指定應用程式閘道前端 IP 資源物件。</span><span class="sxs-lookup"><span data-stu-id="0a46c-130">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="0a46c-131">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0a46c-131">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="0a46c-132">指定應用程式閘道前端 IP 識別碼。</span><span class="sxs-lookup"><span data-stu-id="0a46c-132">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="0a46c-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="0a46c-133">-FrontendPort</span></span>
<span data-ttu-id="0a46c-134">指定應用程式閘道前端埠物件。</span><span class="sxs-lookup"><span data-stu-id="0a46c-134">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="0a46c-135">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="0a46c-135">-FrontendPortId</span></span>
<span data-ttu-id="0a46c-136">指定應用程式閘道前端埠識別碼。</span><span class="sxs-lookup"><span data-stu-id="0a46c-136">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="0a46c-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="0a46c-137">-HostName</span></span>
<span data-ttu-id="0a46c-138">指定此 Cmdlet 新增 HTTP 聆聽者之主機名稱稱。</span><span class="sxs-lookup"><span data-stu-id="0a46c-138">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="0a46c-139">-HostNames</span><span class="sxs-lookup"><span data-stu-id="0a46c-139">-HostNames</span></span>
<span data-ttu-id="0a46c-140">主機名稱</span><span class="sxs-lookup"><span data-stu-id="0a46c-140">Host names</span></span>

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

### <span data-ttu-id="0a46c-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="0a46c-141">-Name</span></span>
<span data-ttu-id="0a46c-142">指定此命令新增的前端埠名稱。</span><span class="sxs-lookup"><span data-stu-id="0a46c-142">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="0a46c-143">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="0a46c-143">-Protocol</span></span>
<span data-ttu-id="0a46c-144">指定 HTTP 聆聽者通訊協定。</span><span class="sxs-lookup"><span data-stu-id="0a46c-144">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="0a46c-145">同時支援 HTTP 和 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="0a46c-145">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="0a46c-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="0a46c-146">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="0a46c-147">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="0a46c-147">-SslCertificate</span></span>
<span data-ttu-id="0a46c-148">指定 HTTP 聆聽者之 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="0a46c-148">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="0a46c-149">如果 HTTPS 是選擇為聆聽者通訊協定，則必須指定。</span><span class="sxs-lookup"><span data-stu-id="0a46c-149">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="0a46c-150">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="0a46c-150">-SslCertificateId</span></span>
<span data-ttu-id="0a46c-151">指定 HTTP 聆聽者之 SSL 憑證識別碼。</span><span class="sxs-lookup"><span data-stu-id="0a46c-151">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="0a46c-152">如果 HTTPS 是選擇為聆聽者通訊協定，則必須指定。</span><span class="sxs-lookup"><span data-stu-id="0a46c-152">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="0a46c-153">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="0a46c-153">-SslProfile</span></span>
<span data-ttu-id="0a46c-154">SslProfile</span><span class="sxs-lookup"><span data-stu-id="0a46c-154">SslProfile</span></span>

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

### <span data-ttu-id="0a46c-155">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="0a46c-155">-SslProfileId</span></span>
<span data-ttu-id="0a46c-156">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="0a46c-156">SslProfileId</span></span>

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

### <span data-ttu-id="0a46c-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a46c-157">CommonParameters</span></span>
<span data-ttu-id="0a46c-158">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0a46c-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a46c-159">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a46c-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a46c-160">輸入</span><span class="sxs-lookup"><span data-stu-id="0a46c-160">INPUTS</span></span>

### <span data-ttu-id="0a46c-161">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a46c-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0a46c-162">輸出</span><span class="sxs-lookup"><span data-stu-id="0a46c-162">OUTPUTS</span></span>

### <span data-ttu-id="0a46c-163">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a46c-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0a46c-164">筆記</span><span class="sxs-lookup"><span data-stu-id="0a46c-164">NOTES</span></span>

## <span data-ttu-id="0a46c-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a46c-165">RELATED LINKS</span></span>

[<span data-ttu-id="0a46c-166">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0a46c-166">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="0a46c-167">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0a46c-167">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="0a46c-168">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0a46c-168">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="0a46c-169">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0a46c-169">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


