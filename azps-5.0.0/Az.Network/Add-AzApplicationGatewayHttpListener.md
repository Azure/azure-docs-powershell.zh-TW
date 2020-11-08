---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: d3434a650eb09391aa7505f288667aa130401e26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136709"
---
# <span data-ttu-id="24723-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="24723-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="24723-102">摘要</span><span class="sxs-lookup"><span data-stu-id="24723-102">SYNOPSIS</span></span>
<span data-ttu-id="24723-103">將 HTTP 偵聽程式新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="24723-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="24723-104">句法</span><span class="sxs-lookup"><span data-stu-id="24723-104">SYNTAX</span></span>

### <span data-ttu-id="24723-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="24723-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24723-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="24723-106">SetByResource</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24723-107">說明</span><span class="sxs-lookup"><span data-stu-id="24723-107">DESCRIPTION</span></span>
<span data-ttu-id="24723-108">**AzApplicationGatewayHttpListener** Cmdlet 會將 HTTP 偵聽程式新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="24723-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="24723-109">示例</span><span class="sxs-lookup"><span data-stu-id="24723-109">EXAMPLES</span></span>

### <span data-ttu-id="24723-110">範例1：新增 HTTP 偵聽程式</span><span class="sxs-lookup"><span data-stu-id="24723-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="24723-111">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會將 HTTP 監聽器新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="24723-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="24723-112">範例2：新增具有 SSL 的 HTTPS 偵聽程式</span><span class="sxs-lookup"><span data-stu-id="24723-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="24723-113">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="24723-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="24723-114">第二個命令會將使用 HTTPS 通訊協定的監聽器新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="24723-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

### <span data-ttu-id="24723-115">範例3：新增具有 SSL 和主機名稱的 HTTPS 偵聽程式</span><span class="sxs-lookup"><span data-stu-id="24723-115">Example 3: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="24723-116">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="24723-116">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="24723-117">第二個命令會將偵聽程式（使用 HTTPS 通訊協定，以及 SSL 憑證和主機名稱）新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="24723-117">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="24723-118">參數</span><span class="sxs-lookup"><span data-stu-id="24723-118">PARAMETERS</span></span>

### <span data-ttu-id="24723-119">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24723-119">-ApplicationGateway</span></span>
<span data-ttu-id="24723-120">指定此 Cmdlet 新增 HTTP 偵聽程式的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="24723-120">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="24723-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="24723-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="24723-122">應用程式閘道的客戶錯誤</span><span class="sxs-lookup"><span data-stu-id="24723-122">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="24723-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24723-123">-DefaultProfile</span></span>
<span data-ttu-id="24723-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="24723-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24723-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="24723-125">-FirewallPolicy</span></span>
<span data-ttu-id="24723-126">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="24723-126">FirewallPolicy</span></span>

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

### <span data-ttu-id="24723-127">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="24723-127">-FirewallPolicyId</span></span>
<span data-ttu-id="24723-128">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="24723-128">FirewallPolicyId</span></span>

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

### <span data-ttu-id="24723-129">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="24723-129">-FrontendIPConfiguration</span></span>
<span data-ttu-id="24723-130">指定應用程式閘道前端 IP 資源物件。</span><span class="sxs-lookup"><span data-stu-id="24723-130">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="24723-131">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="24723-131">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="24723-132">指定應用程式閘道前端 IP ID。</span><span class="sxs-lookup"><span data-stu-id="24723-132">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="24723-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="24723-133">-FrontendPort</span></span>
<span data-ttu-id="24723-134">指定應用程式閘道的 [前端埠] 物件。</span><span class="sxs-lookup"><span data-stu-id="24723-134">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="24723-135">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="24723-135">-FrontendPortId</span></span>
<span data-ttu-id="24723-136">指定應用程式閘道前端埠 ID。</span><span class="sxs-lookup"><span data-stu-id="24723-136">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="24723-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="24723-137">-HostName</span></span>
<span data-ttu-id="24723-138">指定此 Cmdlet 新增 HTTP 偵聽程式的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="24723-138">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="24723-139">-主機名稱</span><span class="sxs-lookup"><span data-stu-id="24723-139">-HostNames</span></span>
<span data-ttu-id="24723-140">主機名稱</span><span class="sxs-lookup"><span data-stu-id="24723-140">Host names</span></span>

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

### <span data-ttu-id="24723-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="24723-141">-Name</span></span>
<span data-ttu-id="24723-142">指定此命令所新增之前端埠的名稱。</span><span class="sxs-lookup"><span data-stu-id="24723-142">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="24723-143">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="24723-143">-Protocol</span></span>
<span data-ttu-id="24723-144">指定 HTTP 偵聽程式的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="24723-144">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="24723-145">支援 HTTP 和 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="24723-145">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="24723-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="24723-146">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="24723-147">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="24723-147">-SslCertificate</span></span>
<span data-ttu-id="24723-148">指定 HTTP 偵聽程式的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="24723-148">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="24723-149">如果將 HTTPS 選作偵聽程式通訊協定，則必須指定。</span><span class="sxs-lookup"><span data-stu-id="24723-149">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="24723-150">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="24723-150">-SslCertificateId</span></span>
<span data-ttu-id="24723-151">指定 HTTP 偵聽程式的 SSL 憑證 ID。</span><span class="sxs-lookup"><span data-stu-id="24723-151">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="24723-152">如果將 HTTPS 選作偵聽程式通訊協定，則必須指定。</span><span class="sxs-lookup"><span data-stu-id="24723-152">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="24723-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24723-153">CommonParameters</span></span>
<span data-ttu-id="24723-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="24723-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24723-155">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="24723-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24723-156">輸入</span><span class="sxs-lookup"><span data-stu-id="24723-156">INPUTS</span></span>

### <span data-ttu-id="24723-157">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="24723-157">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="24723-158">輸出</span><span class="sxs-lookup"><span data-stu-id="24723-158">OUTPUTS</span></span>

### <span data-ttu-id="24723-159">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="24723-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="24723-160">筆記</span><span class="sxs-lookup"><span data-stu-id="24723-160">NOTES</span></span>

## <span data-ttu-id="24723-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="24723-161">RELATED LINKS</span></span>

[<span data-ttu-id="24723-162">AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="24723-162">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="24723-163">新-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="24723-163">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="24723-164">移除-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="24723-164">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="24723-165">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="24723-165">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)

