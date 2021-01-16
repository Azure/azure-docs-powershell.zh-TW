---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: a6fc3eb16cc82f7a0964e8cd0c1697a083771016
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280505"
---
# <span data-ttu-id="5e397-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5e397-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="5e397-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5e397-102">SYNOPSIS</span></span>
<span data-ttu-id="5e397-103">建立應用程式閘道的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="5e397-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="5e397-104">句法</span><span class="sxs-lookup"><span data-stu-id="5e397-104">SYNTAX</span></span>

### <span data-ttu-id="5e397-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5e397-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-FirewallPolicyId <String>] [-SslProfileId <String>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e397-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5e397-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-SslProfile <PSApplicationGatewaySslProfile>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e397-107">說明</span><span class="sxs-lookup"><span data-stu-id="5e397-107">DESCRIPTION</span></span>
<span data-ttu-id="5e397-108">**新的-AzApplicationGatewayHttpListener** Cmdlet 會建立 Azure 應用程式閘道的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="5e397-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="5e397-109">示例</span><span class="sxs-lookup"><span data-stu-id="5e397-109">EXAMPLES</span></span>

### <span data-ttu-id="5e397-110">範例1：建立 HTTP 監聽程式</span><span class="sxs-lookup"><span data-stu-id="5e397-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="5e397-111">這個命令會建立一個名為 Listener01 的 HTTP 偵聽程式，並將結果儲存在名為 $Listener 的變數中。</span><span class="sxs-lookup"><span data-stu-id="5e397-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="5e397-112">範例2：使用 SSL 建立 HTTP 偵聽程式</span><span class="sxs-lookup"><span data-stu-id="5e397-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="5e397-113">這個命令會建立使用 SSL 卸載的 HTTP 偵聽程式，並在 $SSLCert 01 變數中提供 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="5e397-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="5e397-114">該命令會將結果儲存在名為 $Listener 的變數中。</span><span class="sxs-lookup"><span data-stu-id="5e397-114">The command stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="5e397-115">範例3：使用防火牆原則建立 HTTP 偵聽程式</span><span class="sxs-lookup"><span data-stu-id="5e397-115">Example 3: Create an HTTP listener with firewall-policy</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="5e397-116">這個命令會建立一個名為 Listener01 的 HTTP 偵聽程式，FirewallPolicy 為 $firewallPolicy，並將結果儲存在名為 $Listener 的變數中。</span><span class="sxs-lookup"><span data-stu-id="5e397-116">This command creates an HTTP listener named Listener01, FirewallPolicy as $firewallPolicy and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="5e397-117">範例4：新增具有 SSL 和主機名稱的 HTTPS 偵聽程式</span><span class="sxs-lookup"><span data-stu-id="5e397-117">Example 4: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="5e397-118">這個命令會建立使用 SSL 卸載的 HTTP 偵聽程式，並提供 $SSLCert 01 變數中的 SSL 憑證以及兩個主機名稱。</span><span class="sxs-lookup"><span data-stu-id="5e397-118">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable along with two HostNames.</span></span>
<span data-ttu-id="5e397-119">該命令會將結果儲存在名為 $Listener 的變數中。</span><span class="sxs-lookup"><span data-stu-id="5e397-119">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="5e397-120">參數</span><span class="sxs-lookup"><span data-stu-id="5e397-120">PARAMETERS</span></span>

### <span data-ttu-id="5e397-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e397-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="5e397-122">應用程式閘道的客戶錯誤</span><span class="sxs-lookup"><span data-stu-id="5e397-122">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="5e397-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e397-123">-DefaultProfile</span></span>
<span data-ttu-id="5e397-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5e397-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e397-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="5e397-125">-FirewallPolicy</span></span>
<span data-ttu-id="5e397-126">指定對頂層防火牆原則的物件參考。</span><span class="sxs-lookup"><span data-stu-id="5e397-126">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="5e397-127">您可以使用 New-AzApplicationGatewayWebApplicationFirewallPolicy Cmdlet 來建立物件參考。</span><span class="sxs-lookup"><span data-stu-id="5e397-127">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="5e397-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy 名稱 "wafPolicy1"-ResourceGroup "rgName" 使用上述的 commandlet 建立的防火牆原則，可以在 path 規則層級引用。</span><span class="sxs-lookup"><span data-stu-id="5e397-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="5e397-129">上述命令會建立預設的原則設定和受管理的規則。</span><span class="sxs-lookup"><span data-stu-id="5e397-129">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="5e397-130">使用者可以使用 New-AzApplicationGatewayFirewallPolicySettings 和 New-AzApplicationGatewayFirewallPolicyManagedRules 分別指定 PolicySettings、ManagedRules，而不是預設值。</span><span class="sxs-lookup"><span data-stu-id="5e397-130">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

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

### <span data-ttu-id="5e397-131">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="5e397-131">-FirewallPolicyId</span></span>
<span data-ttu-id="5e397-132">指定現有最上層 web 應用程式防火牆資源的 ID。</span><span class="sxs-lookup"><span data-stu-id="5e397-132">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="5e397-133">您可以使用 Get-AzApplicationGatewayWebApplicationFirewallPolicy Cmdlet 傳回防火牆原則識別碼。</span><span class="sxs-lookup"><span data-stu-id="5e397-133">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="5e397-134">我們擁有 ID 之後，您可以使用 *FirewallPolicyId* 參數，而不是 *FirewallPolicy* 參數。</span><span class="sxs-lookup"><span data-stu-id="5e397-134">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="5e397-135">例如：-FirewallPolicyId/subscriptions/<訂閱識別碼>/resourceGroups/<資源群組-識別碼>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName></span><span class="sxs-lookup"><span data-stu-id="5e397-135">For instance: -FirewallPolicyId  �/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>�</span></span>

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

### <span data-ttu-id="5e397-136">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e397-136">-FrontendIPConfiguration</span></span>
<span data-ttu-id="5e397-137">指定 HTTP 偵聽程式的前端 IP 設定物件。</span><span class="sxs-lookup"><span data-stu-id="5e397-137">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="5e397-138">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5e397-138">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="5e397-139">指定 HTTP 偵聽程式的前端 IP 設定 ID。</span><span class="sxs-lookup"><span data-stu-id="5e397-139">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="5e397-140">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="5e397-140">-FrontendPort</span></span>
<span data-ttu-id="5e397-141">指定 HTTP 偵聽程式的前端埠。</span><span class="sxs-lookup"><span data-stu-id="5e397-141">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="5e397-142">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="5e397-142">-FrontendPortId</span></span>
<span data-ttu-id="5e397-143">指定 HTTP 偵聽程式前端埠物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5e397-143">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="5e397-144">-HostName</span><span class="sxs-lookup"><span data-stu-id="5e397-144">-HostName</span></span>
<span data-ttu-id="5e397-145">指定應用程式閘道 HTTP 監聽器的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="5e397-145">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="5e397-146">-主機名稱</span><span class="sxs-lookup"><span data-stu-id="5e397-146">-HostNames</span></span>
<span data-ttu-id="5e397-147">主機名稱</span><span class="sxs-lookup"><span data-stu-id="5e397-147">Host names</span></span>

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

### <span data-ttu-id="5e397-148">-名稱</span><span class="sxs-lookup"><span data-stu-id="5e397-148">-Name</span></span>
<span data-ttu-id="5e397-149">指定此 Cmdlet 所建立之 HTTP 偵聽程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="5e397-149">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5e397-150">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="5e397-150">-Protocol</span></span>
<span data-ttu-id="5e397-151">指定 HTTP 偵聽程式使用的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="5e397-151">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="5e397-152">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="5e397-152">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: true
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e397-153">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="5e397-153">-SslCertificate</span></span>
<span data-ttu-id="5e397-154">指定 HTTP 偵聽程式的 SSL 憑證物件。</span><span class="sxs-lookup"><span data-stu-id="5e397-154">Specifies the SSL certificate object for the HTTP listener.</span></span>

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

### <span data-ttu-id="5e397-155">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="5e397-155">-SslCertificateId</span></span>
<span data-ttu-id="5e397-156">指定 HTTP 偵聽程式的 SSL 憑證 ID。</span><span class="sxs-lookup"><span data-stu-id="5e397-156">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="5e397-157">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="5e397-157">-SslProfile</span></span>
<span data-ttu-id="5e397-158">SslProfile</span><span class="sxs-lookup"><span data-stu-id="5e397-158">SslProfile</span></span>

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

### <span data-ttu-id="5e397-159">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="5e397-159">-SslProfileId</span></span>
<span data-ttu-id="5e397-160">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="5e397-160">SslProfileId</span></span>

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

### <span data-ttu-id="5e397-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e397-161">CommonParameters</span></span>
<span data-ttu-id="5e397-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5e397-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e397-163">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5e397-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e397-164">輸入</span><span class="sxs-lookup"><span data-stu-id="5e397-164">INPUTS</span></span>

### <span data-ttu-id="5e397-165">所有</span><span class="sxs-lookup"><span data-stu-id="5e397-165">None</span></span>

## <span data-ttu-id="5e397-166">輸出</span><span class="sxs-lookup"><span data-stu-id="5e397-166">OUTPUTS</span></span>

### <span data-ttu-id="5e397-167">PSApplicationGatewayHttpListener 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5e397-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="5e397-168">筆記</span><span class="sxs-lookup"><span data-stu-id="5e397-168">NOTES</span></span>

## <span data-ttu-id="5e397-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e397-169">RELATED LINKS</span></span>

[<span data-ttu-id="5e397-170">附加 AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5e397-170">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="5e397-171">AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5e397-171">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="5e397-172">移除-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5e397-172">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="5e397-173">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5e397-173">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


