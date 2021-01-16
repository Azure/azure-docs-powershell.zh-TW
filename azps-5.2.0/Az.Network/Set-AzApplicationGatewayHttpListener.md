---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 8ce5d01d78b8b434e062b0f33ee41a4cbbce20ed
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278966"
---
# <span data-ttu-id="d618a-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d618a-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="d618a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d618a-102">SYNOPSIS</span></span>
<span data-ttu-id="d618a-103">修改應用程式閘道的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="d618a-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="d618a-104">句法</span><span class="sxs-lookup"><span data-stu-id="d618a-104">SYNTAX</span></span>

### <span data-ttu-id="d618a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d618a-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-SslProfileId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d618a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d618a-106">SetByResource</span></span>
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

## <span data-ttu-id="d618a-107">說明</span><span class="sxs-lookup"><span data-stu-id="d618a-107">DESCRIPTION</span></span>
<span data-ttu-id="d618a-108">**AzApplicationGatewayHttpListener** Cmdlet 會修改 Azure 應用程式閘道的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="d618a-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="d618a-109">示例</span><span class="sxs-lookup"><span data-stu-id="d618a-109">EXAMPLES</span></span>

### <span data-ttu-id="d618a-110">範例1：設定 HTTP 偵聽程式</span><span class="sxs-lookup"><span data-stu-id="d618a-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="d618a-111">第一個命令會從屬於名為 ResourceGroup01 之資源群組的名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="d618a-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d618a-112">第二個命令會將閘道的 HTTP 偵聽程式設定為使用以埠80上的 HTTP 通訊協定儲存在 $FIP 01 中的前端配置。</span><span class="sxs-lookup"><span data-stu-id="d618a-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

### <span data-ttu-id="d618a-113">範例2：新增具有 SSL 和主機名稱的 HTTPS 偵聽程式</span><span class="sxs-lookup"><span data-stu-id="d618a-113">Example 2: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="d618a-114">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="d618a-114">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d618a-115">第二個命令會將偵聽程式（使用 HTTPS 通訊協定，以及 SSL 憑證和主機名稱）新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="d618a-115">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="d618a-116">參數</span><span class="sxs-lookup"><span data-stu-id="d618a-116">PARAMETERS</span></span>

### <span data-ttu-id="d618a-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d618a-117">-ApplicationGateway</span></span>
<span data-ttu-id="d618a-118">指定此 Cmdlet 與 HTTP 偵聽程式關聯的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="d618a-118">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="d618a-119">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="d618a-119">-CustomErrorConfiguration</span></span>
<span data-ttu-id="d618a-120">應用程式閘道的客戶錯誤</span><span class="sxs-lookup"><span data-stu-id="d618a-120">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="d618a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d618a-121">-DefaultProfile</span></span>
<span data-ttu-id="d618a-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d618a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d618a-123">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="d618a-123">-FirewallPolicy</span></span>
<span data-ttu-id="d618a-124">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="d618a-124">FirewallPolicy</span></span>

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

### <span data-ttu-id="d618a-125">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="d618a-125">-FirewallPolicyId</span></span>
<span data-ttu-id="d618a-126">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="d618a-126">FirewallPolicyId</span></span>

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

### <span data-ttu-id="d618a-127">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d618a-127">-FrontendIPConfiguration</span></span>
<span data-ttu-id="d618a-128">指定應用程式閘道的前端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="d618a-128">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="d618a-129">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d618a-129">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="d618a-130">指定應用程式閘道的前端 IP 位址識別碼。</span><span class="sxs-lookup"><span data-stu-id="d618a-130">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="d618a-131">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="d618a-131">-FrontendPort</span></span>
<span data-ttu-id="d618a-132">指定應用程式閘道前端埠。</span><span class="sxs-lookup"><span data-stu-id="d618a-132">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="d618a-133">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="d618a-133">-FrontendPortId</span></span>
<span data-ttu-id="d618a-134">指定應用程式閘道前端埠 ID。</span><span class="sxs-lookup"><span data-stu-id="d618a-134">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="d618a-135">-HostName</span><span class="sxs-lookup"><span data-stu-id="d618a-135">-HostName</span></span>
<span data-ttu-id="d618a-136">指定此 Cmdlet 傳送 HTTP 偵聽程式的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="d618a-136">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="d618a-137">-主機名稱</span><span class="sxs-lookup"><span data-stu-id="d618a-137">-HostNames</span></span>
<span data-ttu-id="d618a-138">主機名稱</span><span class="sxs-lookup"><span data-stu-id="d618a-138">Host names</span></span>

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

### <span data-ttu-id="d618a-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="d618a-139">-Name</span></span>
<span data-ttu-id="d618a-140">指定 HTTP 偵聽程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="d618a-140">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="d618a-141">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="d618a-141">-Protocol</span></span>
<span data-ttu-id="d618a-142">指定 HTTP 偵聽程式使用的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="d618a-142">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="d618a-143">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d618a-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d618a-144">Http</span><span class="sxs-lookup"><span data-stu-id="d618a-144">Http</span></span>
- <span data-ttu-id="d618a-145">Ip-HTTPs</span><span class="sxs-lookup"><span data-stu-id="d618a-145">Https</span></span>

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

### <span data-ttu-id="d618a-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="d618a-146">-RequireServerNameIndication</span></span>
<span data-ttu-id="d618a-147">指定 Cmdlet 是否需要伺服器名稱指示。</span><span class="sxs-lookup"><span data-stu-id="d618a-147">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="d618a-148">此參數可接受的值為： true 或 false。</span><span class="sxs-lookup"><span data-stu-id="d618a-148">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="d618a-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="d618a-149">-SslCertificate</span></span>
<span data-ttu-id="d618a-150">指定 HTTP 偵聽程式的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="d618a-150">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="d618a-151">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="d618a-151">-SslCertificateId</span></span>
<span data-ttu-id="d618a-152">指定 (SSL) HTTP 偵聽程式的憑證 ID 的安全通訊端層。</span><span class="sxs-lookup"><span data-stu-id="d618a-152">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="d618a-153">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="d618a-153">-SslProfile</span></span>
<span data-ttu-id="d618a-154">SslProfile</span><span class="sxs-lookup"><span data-stu-id="d618a-154">SslProfile</span></span>

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

### <span data-ttu-id="d618a-155">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="d618a-155">-SslProfileId</span></span>
<span data-ttu-id="d618a-156">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="d618a-156">SslProfileId</span></span>

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

### <span data-ttu-id="d618a-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d618a-157">CommonParameters</span></span>
<span data-ttu-id="d618a-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d618a-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d618a-159">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d618a-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d618a-160">輸入</span><span class="sxs-lookup"><span data-stu-id="d618a-160">INPUTS</span></span>

### <span data-ttu-id="d618a-161">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d618a-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d618a-162">輸出</span><span class="sxs-lookup"><span data-stu-id="d618a-162">OUTPUTS</span></span>

### <span data-ttu-id="d618a-163">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d618a-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d618a-164">筆記</span><span class="sxs-lookup"><span data-stu-id="d618a-164">NOTES</span></span>

## <span data-ttu-id="d618a-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="d618a-165">RELATED LINKS</span></span>

[<span data-ttu-id="d618a-166">附加 AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d618a-166">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="d618a-167">AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d618a-167">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="d618a-168">新-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d618a-168">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="d618a-169">移除-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d618a-169">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


