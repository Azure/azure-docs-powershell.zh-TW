---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 91e8aef2e5d12a13648132a1c8d6ece9dc4d21cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912341"
---
# <span data-ttu-id="63bcd-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="63bcd-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="63bcd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="63bcd-102">SYNOPSIS</span></span>
<span data-ttu-id="63bcd-103">修改應用程式閘道的 HTTP 聆聽程式。</span><span class="sxs-lookup"><span data-stu-id="63bcd-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="63bcd-104">語法</span><span class="sxs-lookup"><span data-stu-id="63bcd-104">SYNTAX</span></span>

### <span data-ttu-id="63bcd-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="63bcd-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-SslProfileId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="63bcd-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="63bcd-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-SslProfile <PSApplicationGatewaySslProfile>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="63bcd-107">描述</span><span class="sxs-lookup"><span data-stu-id="63bcd-107">DESCRIPTION</span></span>
<span data-ttu-id="63bcd-108">**Set-AzApplicationGatewayHttpListener** Cmdlet 會修改 Azure 應用程式閘道的 HTTP 聆聽程式。</span><span class="sxs-lookup"><span data-stu-id="63bcd-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="63bcd-109">例子</span><span class="sxs-lookup"><span data-stu-id="63bcd-109">EXAMPLES</span></span>

### <span data-ttu-id="63bcd-110">範例 1：設定 HTTP 聆聽者</span><span class="sxs-lookup"><span data-stu-id="63bcd-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="63bcd-111">第一個命令會獲得名為 ApplicationGateway01 的應用程式閘道，該閘道屬於名為 ResourceGroup01 的資源群組，並儲存在$AppGw變數中。</span><span class="sxs-lookup"><span data-stu-id="63bcd-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="63bcd-112">第二個命令會設定閘道的 HTTP 聆聽者，以使用儲存在 $FIP 01 中的前端設定與埠 80 上的 HTTP 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="63bcd-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

### <span data-ttu-id="63bcd-113">範例 2：使用 SSL 和 HostName 新增 HTTPS 聆聽者</span><span class="sxs-lookup"><span data-stu-id="63bcd-113">Example 2: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="63bcd-114">第一個命令會獲得應用程式閘道，並儲存在$AppGw變數。</span><span class="sxs-lookup"><span data-stu-id="63bcd-114">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="63bcd-115">第二個命令會將使用 HTTPS 通訊協定與 SSL 憑證和 HostName 的聆聽者新增到應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="63bcd-115">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="63bcd-116">參數</span><span class="sxs-lookup"><span data-stu-id="63bcd-116">PARAMETERS</span></span>

### <span data-ttu-id="63bcd-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63bcd-117">-ApplicationGateway</span></span>
<span data-ttu-id="63bcd-118">指定此 Cmdlet 與 HTTP 聆聽者進行關聯的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="63bcd-118">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="63bcd-119">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="63bcd-119">-CustomErrorConfiguration</span></span>
<span data-ttu-id="63bcd-120">應用程式閘道的客戶錯誤</span><span class="sxs-lookup"><span data-stu-id="63bcd-120">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="63bcd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63bcd-121">-DefaultProfile</span></span>
<span data-ttu-id="63bcd-122">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="63bcd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63bcd-123">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="63bcd-123">-FirewallPolicy</span></span>
<span data-ttu-id="63bcd-124">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="63bcd-124">FirewallPolicy</span></span>

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

### <span data-ttu-id="63bcd-125">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="63bcd-125">-FirewallPolicyId</span></span>
<span data-ttu-id="63bcd-126">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="63bcd-126">FirewallPolicyId</span></span>

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

### <span data-ttu-id="63bcd-127">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="63bcd-127">-FrontendIPConfiguration</span></span>
<span data-ttu-id="63bcd-128">指定應用程式閘道的前端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="63bcd-128">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="63bcd-129">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="63bcd-129">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="63bcd-130">指定應用程式閘道前端 IP 位址的識別碼。</span><span class="sxs-lookup"><span data-stu-id="63bcd-130">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="63bcd-131">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="63bcd-131">-FrontendPort</span></span>
<span data-ttu-id="63bcd-132">指定應用程式閘道前端埠。</span><span class="sxs-lookup"><span data-stu-id="63bcd-132">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="63bcd-133">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="63bcd-133">-FrontendPortId</span></span>
<span data-ttu-id="63bcd-134">指定應用程式閘道前端埠識別碼。</span><span class="sxs-lookup"><span data-stu-id="63bcd-134">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="63bcd-135">-HostName</span><span class="sxs-lookup"><span data-stu-id="63bcd-135">-HostName</span></span>
<span data-ttu-id="63bcd-136">指定此 Cmdlet 傳送 HTTP 聆聽者至的主機名稱稱。</span><span class="sxs-lookup"><span data-stu-id="63bcd-136">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="63bcd-137">-HostNames</span><span class="sxs-lookup"><span data-stu-id="63bcd-137">-HostNames</span></span>
<span data-ttu-id="63bcd-138">主機名稱</span><span class="sxs-lookup"><span data-stu-id="63bcd-138">Host names</span></span>

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

### <span data-ttu-id="63bcd-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="63bcd-139">-Name</span></span>
<span data-ttu-id="63bcd-140">指定 HTTP 聆聽者的名稱。</span><span class="sxs-lookup"><span data-stu-id="63bcd-140">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="63bcd-141">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="63bcd-141">-Protocol</span></span>
<span data-ttu-id="63bcd-142">指定 HTTP 聆聽者使用的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="63bcd-142">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="63bcd-143">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="63bcd-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="63bcd-144">HTTP</span><span class="sxs-lookup"><span data-stu-id="63bcd-144">Http</span></span>
- <span data-ttu-id="63bcd-145">Https</span><span class="sxs-lookup"><span data-stu-id="63bcd-145">Https</span></span>

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

### <span data-ttu-id="63bcd-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="63bcd-146">-RequireServerNameIndication</span></span>
<span data-ttu-id="63bcd-147">指定 Cmdlet 是否需要伺服器名稱指示。</span><span class="sxs-lookup"><span data-stu-id="63bcd-147">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="63bcd-148">此參數可接受的值為：True 或 False。</span><span class="sxs-lookup"><span data-stu-id="63bcd-148">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="63bcd-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="63bcd-149">-SslCertificate</span></span>
<span data-ttu-id="63bcd-150">指定 HTTP 聆聽者之 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="63bcd-150">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="63bcd-151">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="63bcd-151">-SslCertificateId</span></span>
<span data-ttu-id="63bcd-152">指定安全通訊端層 (SSL) HTTP 聆聽者憑證識別碼。</span><span class="sxs-lookup"><span data-stu-id="63bcd-152">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="63bcd-153">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="63bcd-153">-SslProfile</span></span>
<span data-ttu-id="63bcd-154">SslProfile</span><span class="sxs-lookup"><span data-stu-id="63bcd-154">SslProfile</span></span>

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

### <span data-ttu-id="63bcd-155">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="63bcd-155">-SslProfileId</span></span>
<span data-ttu-id="63bcd-156">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="63bcd-156">SslProfileId</span></span>

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

### <span data-ttu-id="63bcd-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63bcd-157">CommonParameters</span></span>
<span data-ttu-id="63bcd-158">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="63bcd-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63bcd-159">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63bcd-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63bcd-160">輸入</span><span class="sxs-lookup"><span data-stu-id="63bcd-160">INPUTS</span></span>

### <span data-ttu-id="63bcd-161">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63bcd-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="63bcd-162">輸出</span><span class="sxs-lookup"><span data-stu-id="63bcd-162">OUTPUTS</span></span>

### <span data-ttu-id="63bcd-163">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63bcd-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="63bcd-164">筆記</span><span class="sxs-lookup"><span data-stu-id="63bcd-164">NOTES</span></span>

## <span data-ttu-id="63bcd-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="63bcd-165">RELATED LINKS</span></span>

[<span data-ttu-id="63bcd-166">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="63bcd-166">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="63bcd-167">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="63bcd-167">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="63bcd-168">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="63bcd-168">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="63bcd-169">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="63bcd-169">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


